<template>
<div class="flex my-10 mr-8 justify-end h-full items-center text-xl">
     <p>Currently Showing:  </p>
  <select name="filter" @change="fireFilter" v-model="filter" class="ml-2">
       <option value="All"> All products</option>
       <option value="men clothing"> Men's Clothing</option>
       <option value="electronics"> Electronics</option>
       <option value="jewelery"> Jewelleries</option>
       <option value="women clothing"> Women's Clothing</option>

  </select>

</div>
</template>

<script>
export default {
     name:"Filter",
     data(){
          return{
          filter: "All"
          }
     },
     methods:{
          fireFilter(){
               this.$emit('filter', this.filter)
          }
     }

}
</script>

<style>

</style>