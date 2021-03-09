<template>
  <section class='search_bar'>
      <FaSearch />
       <input type="text" placeholder="Search for a product"  v-model="term" @input="search_Function" class="flex-1 border-none">
  </section>
</template>

<script>
import { FaSearch } from 'oh-vue-icons/icons'

export default {
     name:"SearchBar",
     components:{
      FaSearch
     },
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