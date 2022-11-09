<template>
  <!-- <Layout> -->
  <div class="home">
    <div id="loader"></div>
    <section class="home-container">
      <!-- Background -->
      <div class="outer-page personal" :style="{ 'background-image': 'url(' + bg_img + ')' }">
        <div class="inner-page personal">
          <div class="decor"></div>
        </div>
      </div>

      <!-- logo -->
      <div class="logo animated fadeInDown" :style="{ 'background-image': 'url(' + logoMain + ')' }">
        <g-link class="nav__link" to="/">Logo</g-link>
      </div>

      <!-- logo mobile -->
      <div class="m-logo animated fadeInDown">
        <a href="#"><img :src="logoMain" alt="m-logo"/></a>
      </div>

      <!-- mobile navbar -->
      <a class="m-navbar-left animated fadeInDown" href="about.html">
        <span>ABOUT US</span>
      </a>
      <a class="m-navbar-right animated fadeInDown" href="work.html">
        <span>PORTFOLIO</span>
      </a>

      <!-- Title -->
      <div class="table">
        <div class="valign">
          <div class="title-personal">
            <p>Hello, iam</p>
            <h1>{{name}}</h1>
            <p class="title-description">
              {{intro}}
            </p>
            <div class="mt-30">
              <g-link class="btn-link" to="/portfolio">MY WORK</g-link>
            </div>
          </div>
        </div>
      </div>

      <!-- Social Media -->
      <div class="social">
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

    </section>

    <!-- Menu Toggle -->
    <div class="button_container" id="toggle">
      <span class="top"></span>
      <span class="middle"></span>
      <span class="bottom"></span>
    </div>

    <div class="overlay" id="overlay">
      <nav class="overlay-menu">
        <ul>
            <li><g-link class="nav__link" to="/">Home</g-link></li>
            <li><g-link class="nav__link" to="/about">About</g-link></li>
            <li><g-link class="nav__link" to="/portfolio">Work</g-link></li>
          </ul>
      </nav>
    </div>

    <!-- Custom cursor -->
    <div class="cursor-dot-outline"></div>
    <div class="cursor-dot"></div>
  </div>
  <!-- </Layout> -->
</template>

<page-query>

</page-query>

<script>
import home from "../../content/pages/home.json"
import logo from "../../content/pages/logo.json"
export default {
  metaInfo: {
    title: 'Rashmika - Portfolio',
  },
  data(){
    return{
      name: home.name,
      intro: home.intro,
      bg_img: home.bg_img,
      logoMain: logo.logo_main,
      logoMobile: logo.logo_mobile
    }
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
