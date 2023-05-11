
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
          <li>Home
            <div class="line"></div>
          </li>
          <li>About Us
            <div class="line"></div>
          </li>
          <li>Training
            <div class="line"></div>
          </li>
          <li>Packages
            <div class="line"></div>
          </li>
          <li>Blog
            <div class="line"></div>
          </li>
          <li>Contact
            <div class="line"></div>
          </li>
        </ul>
      </div>


      <div class="backdrop d-flex align-items-center">
        <button class="btn" type="button" data-bs-toggle="offcanvas" data-bs-target="#staticBackdrop"
          aria-controls="staticBackdrop">
          <i class="fa-solid fa-bars"></i>

        </button>
        <div class="offcanvas offcanvas-start" data-bs-backdrop="static" tabindex="-1" id="staticBackdrop"
          aria-labelledby="staticBackdropLabel" data-bs-dismiss="offcanvas">
          <div class="offcanvas-body">
            <div>
              <img class="loader" src="loader-gobike.png" alt="">
            </div>
            <div class="contact">
              <h2>Contact Information</h2>
              <span><i class="fa-solid fa-phone"></i></span>
              <p>
                +1 (234) 567 89 10
              </p>
              <span><i class="fa-regular fa-envelope"></i></span>
              <p>
                example@example.com
              </p>
              <span><i class="fa-solid fa-location-dot"></i></span>
              <p>
                New Jersey, USA
              </p>
              <span class="social">
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-instagram"></i>
                <i class="fa-brands fa-twitter"></i>
              </span>
              <span class="copyright">© 2023 - Gobike</span>
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
    font-weight: 500;
    display: block;
  }

  .line {
    width: 5px;
    height: 3px;
    background-color: white;
    transition: width 1s;
  }

  li:hover .line {
    display: block;
    transition-timing-function: ease;
    background-color: black;
    width: 100%;
  }

  .backdrop i {
    font-size: 40px;
  }

  .toggle {
    color: white;
    background-color: black;
    padding: 20px;
    margin-left: 20px;
  }

  .toggle i {
    font-size: 10px;
  }
}

// OFFCANVAS
.offcanvas {
  text-align: center;
  display: flex;

  h2 {
    margin: 10px;
  }

  p {
    font-size: 20px;
  }

  .copyright {
    display: block;
    margin-top: 10px;
  }
}

.offcanvas i {
  margin: 10px;
  font-size: 60px;
  color: white;
  background-color: black;
  padding: 20px;
  border-radius: 10px;
}

.offcanvas-body {
  margin: 20px;

  .social i {
    color: black;
    background-color: white;
    padding: 10px 5px;
  }
}

.loader {
  width: 50%;
  margin-bottom: 10px;
}

::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  background-color: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background-color: #000000;
}
</style>