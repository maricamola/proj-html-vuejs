<script>
import events from '../scss/data/events';

export default {
  name: 'CardsEvents',
  components: {
    events,
  },
  props: {
    image: String,
    title: String,
    date: String,
    time: Number,
    country: String,
    type: String,
  }
}
</script>


<template>
  <div class="card" style="width: 24rem;">
    <span class="date">Numb <br> Mese</span>
    <img :src="image" :alt="bike - event">
    <div class="card-body">
      <h3>{{ title }}</h3>
      <p class="card-text">
        <i class="fa-sharp fa-regular fa-clock"></i> {{ date }} @ {{ time }} - @ {{ date }} @ {{ time }}
      </p>
      <p><i class="fa-solid fa-location-dot"></i> {{ country }} </p>
      <p class="event-type">{{ type }}</p>
    </div>
  </div>
</template>




<style lang="scss" scoped>
@use '../scss/main.scss';
@use '../scss/partials/vars.scss';

.event-type {
  background-color: #F5F5F5;
  padding: 5px 7px;
  display: inline-block;
  line-height: 15px;
  font-weight: 400;
  font-size: 14px;
  border-radius: 4px;
}


.card {
  position: relative;
  margin-bottom: 30px;

  .date {
    position: absolute;
    padding: 15px;
    background-color: white;
    top: 20px;
    left: 20px;
    border-radius: 10px;
  }
}
</style>