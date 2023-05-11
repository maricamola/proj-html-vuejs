<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
// Import Swiper styles
import 'swiper/css';

export default {
  name: 'CyclingTrainings',
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
  <swiper :modules="modules" :slides-per-view="4" :space-between="50"
    :navigation="{ nextEl: '.swiper-button-next', prevEl: '.swiper-button-prev' }" :pagination="{ clickable: true }"
    :scrollbar="{ draggable: true }" @swiper="onSwiper" @slideChange="onSlideChange">
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
    <swiper-slide><img src="training-box-4.jpg" alt="Bike"></swiper-slide>

    <swiper-slide>
      <div class="image-container"> <img src="training-box-1.jpg" alt="Bike">
        <div class="image-text">
          <h5>Riding Lesson</h5>
        </div>
      </div>
    </swiper-slide>

    <swiper-slide><img src="training-box-2.jpg" alt="Bike"></swiper-slide>
    <swiper-slide><img src="training-box-3.jpg" alt="Bike"></swiper-slide>
    <swiper-slide><img src="training-box-5.jpg" alt="Bike"></swiper-slide>
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
  height: 100%;
  object-fit: cover;
  border: 5px solid black;
  filter: brightness(0.5);

  &:hover {
    transition: all 0.5s;
    filter: brightness(0.8);
  }
}

.swiper-button-next,
.swiper-button-prev {
  background-color: black;
  padding: 30px;
  color: white;
  margin: 50px;
}

.image-container {
  position: relative;
}

.image-text {
  color: white;
  position: absolute;
  top: 40px;
  left: 100px;
  transform: translate(-50%, -50%);
}
</style>