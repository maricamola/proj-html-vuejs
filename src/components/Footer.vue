<script>
export default {
  name: 'Footer'
}
</script>

<template>
  <footer>
    <div class="container-fluid d-flex justify-content-between align-items-baseline">

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
    <div class="copyright">© 2023 Gobike - All Rights Reserved.</div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss';
@use '../scss/partials/vars.scss';

footer {
  background-color: black;
  color: white;
  padding: 10px 40px;

  .copyright {
    text-align: center;
  }

  .container-fluid img {
    width: 200px;
  }

  button {
    width: 100%;
  }

  ul li {
    list-style: none;
    margin-bottom: 10px;
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

.subscribe input,
.subscribe button {
  border-radius: 0;
  width: 300px;
  height: 50px;
}

.subscribe span,
input,
button {
  margin: 10px 0;
}

.icons span {
  margin: 10px 0;
}
</style>