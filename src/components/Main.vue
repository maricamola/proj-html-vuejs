<script>
import Timing from './Timing.vue'
import CardsEvents from './CardsEvents.vue'
import Articles from './Articles.vue'
import events from '../scss/data/events';

export default {
  name: 'Main',
  data() {
    return {
      events
    }
  },
  components: {
    CardsEvents,
    Articles,
    Timing
  }
}
</script>

<template>
  <main>
    <!-- Sezione cards timing -->
    <section class="timing">
      <Timing />
    </section>

    <!-- Sezione moving -->
    <section class="moving">
      <div class="container">
        <section class="motion d-flex">
          <div class="gift">

            <span class="circle"><img src="bike-circle.png" alt="bike"></span>
            <span class="player"><img src="bike-player.png" alt="player"></span>

          </div>

          <div class="text">
            <h2> Do you want to be a professional cyclist? </h2>
            <p>
              We offer 6 courses of varying difficulty and beautiful scenery that cyclists of all levels can enjoy. You
              will
              learn cycling from professionals with our competent and experienced staff. You will have a lot of fun with
              our
              amazing space.</p>
            <img src="divider.jpg" alt="divider">
            <h3>Professional Team</h3>
            <p>We make you professional by adding your sincerity as well as professionalism.</p>
            <h3>Professional Trainings</h3>
            <p>We always ride with the best equipment, respecting nature and fun.</p>
            <span>Get to know us →</span>
          </div>
        </section>
      </div>
    </section>

    <!-- Sezione cards swiper -->
    <section class="swiperCards">Cards slider</section>


    <!-- Sezione cards eventi -->
    <section class="eventsCards">
      <div class="title">
        <h1>Don't Miss Our Events!</h1>
        <p>Get the amazing cycling experience.</p>
      </div>

      <div class="container-fluid d-flex justify-content-between">

        <CardsEvents v-for="(event, index) in events" :key="index" :image="event.image" :title="event.title"
          :date="event.date" :time="event.time" :country="event.country" :type="event.type" />

      </div>
    </section>

    <!-- Sezione cards trainers -->
    <section class="trainersCards">Cards profili trainers</section>

    <!-- Sezione cards packages -->
    <section class="packagesCards">Cards pacchetti</section>

    <!-- Sezione cards articles -->
    <section class="articles">
      <Articles />
    </section>

  </main>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss';
@use '../scss/partials/vars.scss';

// PRIMA SECTION - TIMING 

.swiperCards,
.trainersCards,
.packagesCards {
  border: 2px solid black;
  height: 200px;
  background-color: bisque;
}

// section  {
//   padding: 100px;
// }

// SEZIONE MOVING CARDS

.moving .container {
  padding: 80px 0;
}

.motion {
  border: 1px solid black;
  width: 80%;
  margin: 0 auto;

  .gift,
  .text {
    border: 1px solid black;
    width: 50%;
  }

  .gift,
  .circle {
    position: relative;
  }

  .circle img {
    width: 100%;
    animation: spin 15s infinite linear;

    @keyframes spin {
      from {
        transform: rotate(0deg);
      }

      to {
        transform: rotate(360deg);
      }
    }
  }

  .player img {
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
  }
}

.title {
  text-align: center;
  margin-bottom: 40px;

  h3 {
    font-size: 22px;
    line-height: 1.42;
    font-weight: 700;
  }
}

.container-fluid {
  padding: 10px 40px;
  flex-wrap: wrap;
}
</style>