<template>
  <section class='search_bar'>
     <div> SearchIcon </div>
       <input type="text" placeholder="Search for a product"  v-model="term" @input="search_Function" class="flex-1 border-none">
  </section>
</template>

<script>
export default {
     name:"SearchBar",
     props:{
          products:{
               type:Array
          },
     },
     data(){
          return{
               term:""
          }
     },
     methods:{
          search_Function(){
               this.$emit('search', this.term)
          }
     }

}
</script>

<style>

</style>