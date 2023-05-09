<script>
export default {
  name: 'Footer'
}
</script>

<template>
  <footer>
    <div class="container-fluid d-flex">
      <section class="icons d-flex flex-column">
        <span><img src="logo-footer-gobike.png" alt="logo"></span>
        <span><i class="fa-solid fa-location-dot"></i> New Jersey, USA </span>
        <span><i class="fa-solid fa-phone"></i> +1 (234) 567 89 10</span>
        <span><i class="fa-regular fa-envelope"></i> example@example.com</span>
      </section>

      <section class="subscribe">
        <span>
          <h3>Join Our Newsletter</h3>
        </span>
        <span>Subscribe to receive useful information.</span>
        <input class="form-control" type="text" value="Your Email Andress" aria-label="readonly input example" readonly>
        <button type="button" class="btn btn-light">Subscribe →</button>
      </section>

      <section class="trainings">
        <span>
          <h3>Trainings</h3>
        </span>
        <ul>
          <li>Riding Lesson</li>
          <li>Safe Driving</li>
          <li>Mountain Bike</li>
          <li>Trail Drive</li>
          <li>Pedaling</li>
        </ul>
      </section>

      <section class="links">
        <span>
          <h3>Quick Links</h3>
        </span>
        <ul>
          <!-- <i class="fa-solid fa-minus"></i> -->
          <li>Home</li>
          <li>About Us</li>
          <li>Training</li>
          <li>Packages</li>
          <li>Blog</li>
          <li>Contact</li>
        </ul>
      </section>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss';
@use '../scss/partials/vars.scss';

footer {
  background-color: black;
  color: white;
  padding: 100px;

  .container-fluid img {
    width: 20%;
  }

  button {
    width: 100%;
  }

  ul li {
    list-style: none;
  }

  li {
    &:hover {
      color: rgba(255, 255, 255, 0.493);
    }
  }

  li:before {
    content: "-";
    font-family: "Font Awesome 6 Solid";
    margin-right: 10px;
  }
}
</style>