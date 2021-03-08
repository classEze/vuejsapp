<template>
  <Header />
  <Slider/>
  <SearchBar @search="Search" :products="productsArray" :rendered="renderedProducts" />
  <Merchants :products="renderedProducts" />
  <Footer />

</template>

<script>
import Header from './Header'
import Footer from './Footer'
import Slider from './Slider'
import Merchants from './Merchants'
import SearchBar from './SearchBar'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Slider,
    Merchants,
    SearchBar
  },
       data(){
          return {
               productsArray : [],
          }
     },
 created () {
          fetch("https://fakestoreapi.com/products")
          .then(res=>res.json())
          .then(data=> this.productsArray = data)
          .catch(err=> console.log(err))
     },
     computed : {
       renderedProducts() {
        return this.productsArray
       }
     },
     methods: {
       Search(term){
        this.renderedProducts = this.productsArray.filter( product => product.title.indexOf(term) !== -1 )
        
       }
     }


}
</script>
<style>

</style>
