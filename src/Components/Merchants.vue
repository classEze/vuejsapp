<template>
 <h1 class="text-center text-2xl mt-4">Products</h1>
  <section class="grid w-11/12 mx-auto my-6 grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
       <div class="card-container" :key="product.id" v-for="product in products">
         <ProductCard  :product="product" />
            </div>
  </section>
</template>

<script>
import ProductCard from './ProductCard'
export default {
     name:"Merchants",
     components:{
       ProductCard,
     },

     props:{
          products:{
               type:Array
          }
     }

}
</script>


<style>

</style>