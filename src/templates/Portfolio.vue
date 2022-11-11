<template>
  <!-- <Layout> -->
  <div class="work-detail">
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

    <!-- Title -->
    <div class="table">
      <div class="valign">
        <div class="container">
          <div class="row">
            <div class="col-md-6">
              <div class="title-work-detail">
                <h2>{{$page.portfolio.title}}</h2>
                <p class="project">
                  Website Development, UI UX, Branding, Responsive
                  Site, Mobile App & System Development
                </p>
                <div class="dash"></div>
                <p>
                  Nat-nat is a simulated mission made of 8 motion
                  graphic interstitials and 7 WebGL games, each
                  testing the user on a range of STEM skills that are
                  required for the U.S. Army’s most unique career
                  opportunities.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Content -->
    <div class="bg-main mt-full">
      <div class="container">
        <div class="row">
          <div class="col-md-8 offset-md-2 text-center">
            <div class="web-detail">
              <h3>Websites</h3>
              <p
                class="m-each"
                data-aos-once="true"
                data-aos="fade-up"
              >
                Nat-nat website was also developed by us. We focused
                on improving and optimizing the navigation, making it
                more intuitive and functional, highlighting videos and
                attractive images of the complex, creating a
                differentiated and pleasant experience.
              </p>

              <div
                class="image-work"
                data-aos-once="true"
                data-aos="fade-up"
              >
                <img
                  class="img-fluid"
                  src="img/work-detail/1.png"
                  alt="3"
                />
              </div>

              <div
                class="m-each"
                data-aos-once="true"
                data-aos="fade-up"
              >
                <a href="#" class="btn-link">launch Website</a>
              </div>

              <div data-aos-once="true" data-aos="fade-up">
                <img
                  class="img-fluid"
                  src="img/work-detail/2.jpg"
                  alt="2"
                />
              </div>

              <p class="m-each">
                Nat-nat website was also developed by us. We focused
                on improving and optimizing the navigation, making it
                more intuitive and functional, highlighting videos and
                attractive images of the complex, creating a
                differentiated and pleasant experience.
              </p>

              <div
                class="image-work"
                data-aos-once="true"
                data-aos="fade-up"
              >
                <img
                  class="img-fluid"
                  src="img/work-detail/3.jpg"
                  alt="2"
                />
              </div>

              <div
                class="image-work"
                data-aos-once="true"
                data-aos="fade-up"
              >
                <img
                  class="img-fluid"
                  src="img/work-detail/4.jpg"
                  alt="2"
                />
              </div>
            </div>
            <!-- Navigation Bottom -->
            <ul class="prev-nex-btn">
              <li><a href="work-detail.html">Previous Project</a></li>
              <li><a href="work-detail.html">Next Project</a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <!-- Button Back -->
    <div class="btn-back">
      <g-link class="txt" to="/portfolio">Back to works </g-link>
      <span>
        <a href=""><img src="../img/work-detail/back.png" alt="hh"/></a>
      </span>
    </div>

    <!-- Cursor -->
    <div class="cursor-dot-outline"></div>
    <div class="cursor-dot"></div>
  </div>
  <!-- </Layout> -->
</template>

<script>
export default {
  metaInfo: {
    title: 'hd'
  },
  mounted() {
    const custom = document.createElement('script');
    custom.setAttribute('src', '../../../js/custom.js');
    custom.async = true;
    document.head.appendChild(custom);
  },
};
</script>

<page-query>
    query Postfolio ($id: ID!) {
        portfolio: portfolio (id: $id) {
            title
        }
    }
  </page-query>

<style>
@import '../css/plugin.css';
@import '../css/style.css';
@import '../css/responsive.css';
</style>
