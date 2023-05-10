<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import { Navigation } from 'swiper';


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
}
</script>


<template>
  <Header />

  <Main />

  <Footer />
</template>


<style lang="scss">
@use './scss/main.scss';
</style>