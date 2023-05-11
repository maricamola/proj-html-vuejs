<script>
import plans from '../scss/data/plans';

export default {
  name: 'Packs',
  components: {
    plans
  },
  props: {
    type: String,
    price: Number
  }
}
</script>



<template>
  <div class="maincontainer">
    <div class="thecard">

      <div class="thefront">
        <span><i class="fa-sharp fa-regular fa-handshake"></i></span>
        <!-- <span><i class="fa-sharp fa-solid fa-helmet-safety"></i></span> -->
        <!-- <span><i class="fa-solid fa-crown"></i></span> -->

        <h1>{{ type }}</h1>
        <p>Learn to ride a bike from the professionals.</p>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">✓ Phone Mountaineer bike training</li>
          <li class="list-group-item">✓ Remote Excellent bike service</li>
          <li class="list-group-item">✓ Onsite Safe cycling training</li>
          <li class="list-group-item">✗ Saafety helmet on bike</li>
          <li class="list-group-item">✗ Free bikes for children</li>
        </ul>
      </div>

      <div class="theback">
        <h1>{{ type }}</h1>
        <span>{{ price }}</span>
        <div><button type="button" class="btn btn-dark">Send Request!</button></div>
      </div>

    </div>
  </div>
</template>



<style lang="scss" scoped>
.maincontainer {
  width: 300px;
  height: 550px;
  background: none;
  text-align: center;
  display: flex;
  align-items: center;

}

.thecard {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 10px;
  transform-style: preserve-3d;
  transition: all 0.8s ease;
}

.thecard:hover {
  transform: rotateY(180deg);
}

h1,
p {
  margin: 10px;
}

.thefront {
  position: absolute;
  padding-top: 20px;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 10px;
  backface-visibility: hidden;
  overflow: hidden;
  background: black;
  color: white;
}

.theback {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 10px;
  backface-visibility: hidden;
  overflow: hidden;
  background: black;
  color: white;
  text-align: center;
  transform: rotateY(180deg);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.btn-dark {
  padding: 20px;
  color: white;
  background-color: black;
  border: 1px solid white;
  border-radius: 0;
  margin: 10px;

  &:hover {
    background-color: black;
    border: 1px solid white;
  }
}
</style>