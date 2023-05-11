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
    <swiper-slide>
      <div class="image-container"> <img src="training-box-4.jpg" alt="Bike">
        <div class="image-text">
          <h5>Trail Drive</h5>
        </div>
      </div>
    </swiper-slide>

    <swiper-slide>
      <div class="image-container"> <img src="training-box-1.jpg" alt="Bike">
        <div class="image-text">
          <h5>Riding Lesson</h5>
        </div>
      </div>
    </swiper-slide>

    <swiper-slide>
      <div class="image-container"> <img src="training-box-2.jpg" alt="Bike">
        <div class="image-text">
          <h5>Safe Driving</h5>
        </div>
      </div>
    </swiper-slide>

    <swiper-slide>
      <div class="image-container"> <img src="training-box-3.jpg" alt="Bike">
        <div class="image-text">
          <h5>Mountain Bike</h5>
        </div>
      </div>
    </swiper-slide>

    <swiper-slide>
      <div class="image-container"> <img src="training-box-5.jpg" alt="Bike">
        <div class="image-text">
          <h5>Pedaling</h5>
        </div>
      </div>
    </swiper-slide>

    <swiper-pagination class="swiper-pagination"></swiper-pagination>
    <div class="swiper-button-container">
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </div>
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

//BUTTON NEXT - BUTTON PREV
.swiper-button-container {
  display: flex;
  align-items: center;
  justify-content: center;
}

.swiper-button-next,
.swiper-button-prev {
  position: relative;
  background-color: white;
  padding: 30px;
  color: black;
  margin: 50px 20px;
  border: 1px solid black;
}

//PER IL TESTO ALL'INTERNO DELL'IMG
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