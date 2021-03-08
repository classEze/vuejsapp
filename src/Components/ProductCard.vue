<template>
  <img :src="product.image" alt="Product" class=" object-contain mx-auto h-4/6 w-4/6 mt-2 ">
  <div class="flex-1 bg-black text-white pt-6 px-4">
  <p><span class="font-bold" >  Product : </span>  {{product.title}} </p>
  <p><span class="font-bold">  Category: </span>  {{product.category}} </p>
  </div>
</template>

<script>
export default {
     name:"ProductsCard",

     props:{
          product:{
               type:Object
          }
     }
}
</script>
<style>

</style>