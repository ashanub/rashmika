<template>
  <!-- <Layout> -->
  <div class="about">
    <div id="loader"></div>

    <!-- main-background -->
    <div class="main-detail-bg">
      <!-- mouse animation -->
      <a href="#">
        <div id="mouse-scroll">
          <div class="mouse">
            <div class="mouse-in"></div>
          </div>
          <div>
            <span class="down-arrow-1"></span>
            <span class="down-arrow-2"></span>
            <span class="down-arrow-3"></span>
          </div></div
      ></a>
    </div>

    <!-- Content -->
    <div class="table">
      <div class="valign">
        <div class="container">
          <div class="row">
            <!-- title -->
            <div class="col-md-12">
              <div
                class="title-about"
                data-aos-once="true"
                data-aos="fade-up"
                data-aos-delay="200"
              >
                <h2>
                  {{topDesc}}
                </h2>
                <div class="dash"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="bg-white mt-full">
      <div class="container">
        <!-- What we do -->
        <div class="row m-each">
          <div class="col-lg-4 mt-30">
            <h3
              data-aos-once="true"
              data-aos="fade-up"
              data-aos-delay="100"
            >
              My Skills
            </h3>
          </div>
          <div class="col-md-6 col-lg-4  mt-30">
            <div
              class="ww-content"
              data-aos="fade-up"
              data-aos-delay="200"
              data-aos-once="true"
            >
              <div class="icon hov">
                <i class="fab fa-connectdevelop"></i>
              </div>
              <h5>Development</h5>
              <ul class="list-services">
                <li>front-end</li>
                <li>Back-end</li>
                <li>App Developmnet</li>
                <li>Mobile Hybrid</li>
              </ul>
            </div>
          </div>
          <div class="col-md-6 col-lg-4  mt-30">
            <div
              class="ww-content"
              data-aos="fade-up"
              data-aos-delay="300"
              data-aos-once="true"
            >
              <div class="icon hov">
                <i class="fab fa-connectdevelop"></i>
              </div>
              <h5>UI UX Design</h5>
              <ul class="list-services">
                <li>WEB DEsign</li>
                <li>mobile</li>
                <li>rapid prototype</li>
                <li>Platform</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Client -->
    <div class="bg-main">
      <div class="container">
        <div class="row">
          <!-- Email to -->
          <div
            class="col-md-12 col-lg-8 offset-lg-2 text-center m-each"
          >
            <div
              class="email"
              data-aos-once="true"
              data-aos="fade-up"
              data-aos-delay="200"
            >
              <h2>
                Ready to inject style into your next project ?
              </h2>
              <a id="zoom-fade" href="mailto:mailr@example.com"
                >HELLO@EMBUN.CO</a
              >
            </div>
          </div>
        </div>
      </div>

      <!-- Address -->
      <div class="footer">
        <div class="container">
          <div class="row">
            <div class="col-md-4 mt-30">
              <i class="fas fa-envelope"></i>
              <h4>Say Hello</h4>
              <p>example@mail.com</p>
            </div>
            <div class="col-md-4 mt-30">
              <div class="address">
                <i class="fas fa-phone"></i>
                <h4>Telephone</h4>
                <p>+20 ( 432 ) 3476 3479</p>
              </div>
            </div>
            <div class="col-md-4 mt-30">
              <div class="address">
                <i class="fas fa-map-marker"></i>
                <h4>Address</h4>
                <p>
                  75 New York - Bourbon Street 10/555 Klaten - Central
                  Java
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- logo -->
    <div class="logo animated fadeInDown">
      <g-link class="nav__link" to="/">Logo</g-link>
    </div>

    <!-- logo mobile -->
    <div class="m-logo animated fadeInDown">
      <a href="index.html"
        ><img src="img/mobile-logo.png" alt="m-logo"
      /></a>
    </div>

    <!-- mobile navbar -->
    <a class="m-navbar-left animated fadeInDown" href="about.html">
      <span>ABOUT US</span>
    </a>
    <a class="m-navbar-right animated fadeInDown" href="work.html">
      <span>PORTFOLIO</span>
    </a>

    <!-- Social Media -->
    <div class="social animated fadeInUp">
      <ul>
        <li>
          <a href="#"><i class="fab fa-behance"></i></a>
        </li>
        <li>
          <a href="#"><i class="fab fa-dribbble"></i></a>
        </li>
        <li>
          <a href="#"><i class="fab fa-instagram"></i></a>
        </li>
        <li>
          <a href="#"><i class="fab fa-medium"></i></a>
        </li>
      </ul>
    </div>

    <!-- Navbar Toggle -->
    <div class="button_container animated fadeInDown" id="toggle">
      <span class="top"></span>
      <span class="middle"></span>
      <span class="bottom"></span>
    </div>

    <div class="overlay" id="overlay">
      <nav class="overlay-menu">
        <ul>
          <li><g-link class="nav__link" to="/">Home</g-link></li>
          <li>
            <g-link class="nav__link" to="/about">About</g-link>
          </li>
          <li>
            <g-link class="nav__link" to="/portfolio">Work</g-link>
          </li>
        </ul>
      </nav>
    </div>

    <!-- Cursor -->
    <div class="cursor-dot-outline"></div>
    <div class="cursor-dot"></div>
  </div>
  <!-- </Layout> -->
</template>

<script>
import about from '../../content/pages/about.json';
export default {
  metaInfo: {
    title: 'About us',
  },
  data() {
    return {
      topDesc: about.top_desc,
      bgImg: about.bg_img,
      intro: about.intro,
      email: about.email,
      phone: about.phone,
      address: about.address,
    };
  },
  mounted() {
    const custom = document.createElement('script');
    custom.setAttribute('src', '../js/custom.js');
    custom.async = true;
    document.head.appendChild(custom);
  },
};
</script>
<style>
@import '../css/plugin.css';
@import '../css/style.css';
@import '../css/responsive.css';
</style>
