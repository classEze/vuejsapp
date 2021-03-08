<template>
  <section class="mt-24">
     <Swiper
    :slides-per-view="1"
    :space-between="20 "
    pagination
    autoplay
    >
<SwiperSlide class="relative"> 
     <img src="/image1.png" class=" slider_image " alt="image">
</SwiperSlide>>
<SwiperSlide class="relative"> 
     <img src="/image2.png" class=" slider_image " alt="image">
</SwiperSlide>
<SwiperSlide class="relative"> 
     <img src="/image3.png" class=" slider_image " alt="image">
</SwiperSlide>>
     </Swiper>   
 </section>
</template>
<script>
import {Swiper, SwiperSlide} from 'swiper/vue'
import SwiperCore, { Pagination, Autoplay} from 'swiper'
import "swiper/swiper-bundle.css"
SwiperCore.use([ Pagination, Autoplay])

export default {
     name: "Slider",
     components:{
          Swiper,
          SwiperSlide
     }
}
</script>
<style >
</style>