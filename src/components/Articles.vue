<script>
export default {
  name: 'Articles'
}
</script>




<template>
  <div class="card" style="width: 18rem;">
    <div class="card-body">
      <img src="news-bike5.jpg" style="width: 100%;">
      <span>22/06/2023 - Bike</span>
      <h5 class=" card-title">Special title treatment</h5>
      <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
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
    border-radius: 0px;
    cursor: pointer;
  }
}
</style>