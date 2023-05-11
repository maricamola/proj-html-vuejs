<script>
import Timing from './Timing.vue'
import CyclingTrainings from './CyclingTrainings.vue'
import CardsEvents from './CardsEvents.vue'
import TrainerProfiles from './TrainerProfiles.vue'
import Articles from './Articles.vue'
import stories from '../scss/data/stories';
import events from '../scss/data/events';
import bikers from '../scss/data/bikers';


export default {
  name: 'Main',
  data() {
    return {
      events,
      stories,
      bikers,
    }
  },
  components: {
    CardsEvents,
    Articles,
    Timing,
    TrainerProfiles,
    CyclingTrainings
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
            <div class="subscribe"><button>Get to know us →</button></div>
          </div>
        </section>
      </div>
    </section>

    <!-- Sezione cards swiper -->
    <section class="swiperCards">
      <div class="title">
        <h1>Our Professional Cycling Trainings</h1>
        <p>Learn from the mountain biking expert.</p>
      </div>

      <div class="container-fluid">
        <CyclingTrainings />
      </div>
    </section>


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
    <section class="trainersCards">
      <div class="title">
        <h1>Our Expert Trainers</h1>
        <p>Learn to ride a bike from the experts.</p>
      </div>
      <div class="container-fluid d-flex justify-content-between">

        <TrainerProfiles v-for="(biker, index) in bikers" :key="index" :image="biker.image" :name="biker.name"
          :work="biker.work" />

      </div>
    </section>

    <!-- Sezione cards packages -->
    <section class="packagesCards">Cards pacchetti</section>


    <!-- Sezione cards articles -->
    <section class="articles">
      <div class="title">
        <h2> Resent New & Articles </h2>
        <p>
          Important information about bike </p>
      </div>
      <div class="container-fluid d-flex justify-content-between">
        <Articles v-for="(story, index) in stories" :key="index" :image="story.image" :date="story.date"
          :title="story.title" :text="story.text" />
      </div>

    </section>

  </main>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss';
@use '../scss/partials/vars.scss';

//PER TUTTE LE SECTION
.title {
  text-align: center;
  margin-bottom: 40px;

  h3 {
    font-size: 22px;
    line-height: 1.42;
    font-weight: 700;
  }
}

// PRIMA SECTION - TIMING 
.packagesCards {
  border: 2px solid black;
  height: 200px;
  background-color: bisque;
}

// SEZIONE MOVING CARDS

.moving .container {
  padding: 80px 0;

  .subscribe button {
    color: white;
    padding: 20px;
    background-color: black;
    border: none;
  }
}

.motion {
  width: 80%;
  margin: 0 auto;

  .gift,
  .text {
    width: 50%;
  }

  .text {
    padding: 30px;
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

// SEZIONE CYCLING TRAININGS/CARDS SWIPER
.swiperCards {
  padding: 100px 0;
}

// SEZIONE ARTICOLI 

.articles,
.trainersCards {
  background-color: #FBFBFB;
  padding: 100px 0;
}

.container-fluid {
  padding: 10px 40px;
  flex-wrap: wrap;
}
</style>