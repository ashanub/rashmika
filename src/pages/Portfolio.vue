<template>
  <!-- <Layout> -->
  <div class="work">
    <div id="loader"></div>

    <!-- Side Navbar -->
    <nav class="work-nav">
      <div class="table">
        <div class="valign">
          <a
            class="item-menu active"
            :data-menuanchor="pageAnchors[index]"
            :href="pageLinks[index]"
            v-for="(edge, index) in $page.portfolios.edges"
            :key="edge.node.id"
          >
            <span class="text">{{ edge.node.title }}</span></a
          >
        </div>
      </div>
    </nav>

    <!-- Work List -->
    <div class="pagepiling">
      <!-- Work 01 -->
      <div
        :class="'section work-' + (index + 1)"
        v-for="(edge, index) in $page.portfolios.edges"
        :key="edge.node.id"
      >
        <div class="layer">
          <!-- background -->
          <div
            :class="'prx bg-work-' + (index + 1)"
            :id="'--' + (index + 1)"
            :style="{ 'background-image': 'url(' +edge.node.path + edge.node.showcase.bg_img + ')' }"
          >
            <!-- Work Image -->
            <div
              :class="'img-obj-' + (index + 1)"
              data-depth="0.20"
            ></div>
          </div>
        </div>
        <div class="container">
          <div class="row">
            <div class="col-md-8">
              <div class="title-work animated fadeInUp delay-0.5s">
                <a href="work-detail.html">
                  <h3 id="zoom-fade">{{ edge.node.title }}</h3>
                  <p class="sub">
                    {{edge.node.short_description}}
                  </p>
                  <h4 class="btn-detail">Work detail</h4></a
                >
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
    <div class="social">
      <ul>
        <li>
          <a href="#"><i class="fab fa-twitter"></i></a>
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
          <li>
            <g-link class="nav__link" to="/about">About</g-link>
          </li>
          <li>
            <g-link class="nav__link" to="/portfolio">Work</g-link>
          </li>
        </ul>
      </nav>
    </div>

    <!-- Bottom Navigation Mobile-->
    <a class="bottom-nav-m">Next project</a>
    <div class="cursor-dot-outline"></div>
    <div class="cursor-dot"></div>
  </div>
  <!-- </Layout> -->
</template>
<page-query>
  query{
    portfolios: allPortfolio{
      edges{
        node{
          id
          title
          path
          short_description
          long_description
          showcase{
            add_to_showcase
            bg_img
            float_img
          }
        }
      }
    }
  }
</page-query>

<script>
export default {
  metaInfo: {
    title: 'About us',
  },
  data() {
    return {
      pageLinks: [
        '#firstPage',
        '#secondPage',
        '#thirdPage',
        '#fourhtPage',
        '#fifthPage',
        '#sixthPage',
      ],
      pageAnchors: [
        'firstPage',
        'secondPage',
        'thirdPage',
        'fourhtPage',
        'fifthPage',
        'sixthPage',
      ],
    };
  },
  mounted() {
    const custom = document.createElement('script');
    custom.setAttribute('src', '../js/work.js');
    custom.async = true;
    document.head.appendChild(custom);
  },
};
</script>
<style>
@import '../css/plugin.css';
@import '../css/plugin/jquery.pagepiling.min.css';
@import '../css/style.css';
@import '../css/responsive.css';
</style>
