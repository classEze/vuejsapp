<template>
<div class="header">
<img src="/logo.png" class="h-5/6 w-auto object-contain" alt="">
 <GiHamburgerMenu class='text-3xl text-white' />
</div>  
</template>

<script>    
import { GiHamburgerMenu } from 'oh-vue-icons/icons'
export default {
     name:"Header",
     components: {
    GiHamburgerMenu
}


}
</script>

<style>

</style>