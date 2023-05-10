<script>
import stories from '../scss/data/stories';

export default {
  name: 'Articles',
  components: {
    stories
  },
  props: {
    image: String,
    date: String,
    title: String,
    text: String,
  }
}
</script>


<template>
  <div class="card" style="width: 18rem;">
    <div class="card-body">
      <img :src="image" style="width: 100%;" :alt="article">
      <span>{{ date }} - Bike</span>
      <h5 class="card-title">{{ title }}</h5>
      <p class="card-text">{{ text }}</p>
      <a href="#" class="btn">More</a>
    </div>
  </div>
</template>




<style lang="scss" scoped>
@use '../scss/main.scss';
@use '../scss/partials/vars.scss';

.card {
  text-align: center;

  h5 {
    margin: 10px 0;
  }

  .btn {
    background-color: black;
    color: white;
    padding: 20px 40px;
    border-radius: 5px;
    cursor: pointer;
  }
}
</style>