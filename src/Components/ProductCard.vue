<template>
  <img :src="product.image" alt="Product" class=" h-5/6 w-5/6 mt-2 ">
  {{product.category}}
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