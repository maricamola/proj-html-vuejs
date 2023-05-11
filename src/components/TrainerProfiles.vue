<script>
import bikers from '../scss/data/bikers';


export default {
  name: 'TrainerProfiles',
  components: {
    bikers
  },
  props: {
    image: String,
    name: String,
    work: String,
  }
}
</script>


<template>
  <div class="card" style="width: 20rem;">
    <img :src="image" :class="card - img - top" :alt="Biker">
    <div class="card-body">
      <div class="card-text">
        <ul>
          <li>
            <h6>{{ name }}</h6>
          </li>
          <li>{{ work }}</li>
          <li>
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-instagram"></i>
            <i class="fa-brands fa-twitter"></i>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
.card {
  border: 10px solid rgb(255, 255, 255);
  color: white;
  text-align: center;

  img {
    position: relative;
  }

  .card-body {
    width: 100%;
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: black;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 10px;
  }

  li i {
    font-size: 16px;
    margin: 5px;
  }
}
</style>