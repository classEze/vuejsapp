<template>
  <Header />
  <Slider />
  <SearchBar @search="Search" :products="productsArray" :rendered="renderedProducts" />
   <Filter @filter="filter_Items" />
  <Merchants :products="renderedProducts" />
  <Footer />
</template>

<script>
import Header from './Header'
import Footer from './Footer'
import Slider from './Slider'
import Merchants from './Merchants'
import SearchBar from './SearchBar'
import Filter from './Filter.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Slider,
    Merchants,
    SearchBar,
    Filter
  },
       data(){
          return {
               productsArray : [],
               renderedProducts: []
          }
     },
 created () {
          fetch("https://fakestoreapi.com/products")
          .then(res=>res.json())
          .then(data=>{
            this.productsArray = data
           this.renderedProducts = data
          })
          .catch(err=> console.log(err))
     },
     methods: {
       Search(term){
         console.log(term)
        this.renderedProducts = this.productsArray.filter( product => product.title.toLowerCase().indexOf(term.toLowerCase()) !== -1 )
        
       },
       filter_Items(category) {
        if(category == "All") return this.renderedProducts = this.productsArray
       this.renderedProducts = this.productsArray.filter( product => product.category === category )

       }
     }


}
</script>
<style>

</style>
