<template>
<div class="footer">
      &copy; 9PayMerchant, {{today}}
</div>
  
</template>

<script>
export default {
     name:"Footer", 

     data(){
           return{
            today:new Date().getUTCFullYear()
           }
     }

}
</script>

<style>

</style>