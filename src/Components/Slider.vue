<template>
  <section class="mt-24">
     <Swiper
    :slides-per-view="3"
    :space-between="20 "
    pagination
    autoplay
    centeredSlide
    >
<SwiperSlide> 
     <img src="/image1.png" class="w-11/12 mx-auto object-fill" alt="image">
</SwiperSlide>>
<SwiperSlide> 
     <img src="/image2.png" class="w-11/12 h-11/12 mx-auto object-fill" alt="image">
</SwiperSlide>
<SwiperSlide> 
     <img src="/image3.png" class="w-11/12 h-11/12 mx-auto object-fill" alt="image">
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