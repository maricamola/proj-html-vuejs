<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
// Import Swiper styles
import 'swiper/css';

export default {
  name: 'Timing',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log('slide change');
    };
    return {
      onSwiper,
      onSlideChange,
    };
  },
  mounted() {
    // const mySwiper = new Swiper('.swiper-container', {
    //   // opzioni swiper
    // });
  }
}
</script>



<template>
  <swiper :modules="modules" :slides-per-view="1" :space-between="50"
    :navigation="{ nextEl: '.swiper-button-next', prevEl: '.swiper-button-prev' }" :pagination="{ clickable: true }"
    :scrollbar="{ draggable: true }" @swiper="onSwiper" @slideChange="onSlideChange">
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
    <swiper-slide><img src="slider-bike-4.jpg" alt="Bike"></swiper-slide>
    <swiper-slide><img src="slider-bike-9.jpg" alt="Bike"></swiper-slide>
    <swiper-slide><img src="slider-bike-12.jpg" alt="Bike"></swiper-slide>
  </swiper>
</template>




<style lang="scss" scoped>
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.swiper-button-next,
.swiper-button-prev {
  background-color: black;
  padding: 30px;
  color: white;
  margin: 50px;
}
</style>