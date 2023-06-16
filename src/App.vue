<script setup>
import wrapped from './components/wrapped.vue'
import countries from './components/countries.vue'
//import { Swiper, SwiperSlide } from 'swiper/vue';
</script>

<template>
  <div  class="scroll-container">
    <div id="wrapped" class="scroll-area">
      <wrapped />
    </div>
    <div id="countries" class="scroll-area">
      <countries/>
    </div>
  </div>
</template>

<style>
@import './assets/main.css';
@import 'swiper/css';


body {
  overflow-x: hidden;
}

.scroll-container {
  flex-basis: 50%;
  max-height: 98vh;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
}

.scroll-area {
  padding-top: 2%;
  max-height: 100vh;
  scroll-snap-align: start;
  display: flex;
  flex-flow: column;
  justify-content: center;
}

.blur {
  filter: blur(1.5rem);
}
</style>

