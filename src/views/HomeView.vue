<template>
  <main>

  </main>
</template>

<script setup>



// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
import SwiperCore, { Pagination, Autoplay } from 'swiper';
// Import Swiper styles
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/autoplay'
SwiperCore.use([ Pagination, Autoplay])
const autoplay= {
  delay: 3500,
  disableOnInteraction: false
}

</script>
