
<script>
export default {
  name: 'Header'
}
</script>

<template>
  <header>
    <div class="container-fluid d-flex justify-content-between align-items-center">
      <img src="logo-gobike.png" alt="logo">

      <div class="navbar d-flex">
        <ul>
          <li>Home</li>
          <li>About Us</li>
          <li>Training</li>
          <li>Packages</li>
          <li>Blog</li>
          <li>Contact</li>
        </ul>
      </div>


      <div class="backdrop d-flex align-items-center">
        <button class="btn" type="button" data-bs-toggle="offcanvas" data-bs-target="#staticBackdrop"
          aria-controls="staticBackdrop">
          <i class="fa-solid fa-bars"></i>

        </button>

        <div class="offcanvas offcanvas-start" data-bs-backdrop="static" tabindex="-1" id="staticBackdrop"
          aria-labelledby="staticBackdropLabel">
          <div class="offcanvas-header">
            <h5 class="offcanvas-title" id="staticBackdropLabel">Offcanvas</h5>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
          </div>
          <div class="offcanvas-body">
            <div>
              I will not close if you click outside of me.
            </div>
          </div>
        </div>

        <!-- Bottone con immagine -->
        <div class="toggle">
          <span>
            <h6>Upcoming Events <i class="fa-solid fa-arrow-right"></i></h6>
          </span>
        </div>
      </div>

    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss';
@use '../scss/partials/vars.scss';

header {
  position: fixed;
  height: 90px;
  width: 100%;
  z-index: 999;
  background-color: white;
  display: flex;
  justify-content: center;

  .container-fluid {
    align-items: center;
    padding: 10px 40px;
  }

  img {
    width: 15%
  }

  .navbar ul {
    list-style: none;
    display: flex;
  }

  ul li {
    margin: 0 10px;
    font-size: 18px;
  }

  .backdrop i {
    font-size: 40px;
  }

  .toggle {
    border: 1px solid black;
    padding: 20px;
  }

  .toggle i {
    font-size: 10px;
  }
}
</style>