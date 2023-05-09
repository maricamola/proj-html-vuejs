<script>
export default {
  name: 'Main'
}
</script>

<template>
  <main>
    <section>Foto grande con timing</section>

    <div class="container">
      <section class="motion d-flex">
        <div class="gift">

          <span class="circle"><img src="bike-circle.png" alt="bike"></span>
          <span class="player"><img src="bike-player.png" alt="player"></span>

        </div>

        <div class="text">
          <h2> Do you want to be a professional cyclist? </h2>
          <p>
            We offer 6 courses of varying difficulty and beautiful scenery that cyclists of all levels can enjoy. You will
            learn cycling from professionals with our competent and experienced staff. You will have a lot of fun with our
            amazing space.</p>
          <img src="" alt="">
          <h3>Professional Team</h3>
          <p>We make you professional by adding your sincerity as well as professionalism.</p>
          <h3>Professional Trainings</h3>
          <p>We always ride with the best equipment, respecting nature and fun.</p>
          <span><Button>Get to know us →</Button></span>
        </div>
      </section>
    </div>







    <section>Cards slider</section>
    <section>Cards events stile bootstrap</section>
    <section>Cards profili trainers</section>
    <section>Cards pacchetti</section>
  </main>
</template>

<style lang="scss" scoped>
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
</style>