<template>
  <!-- <Layout> -->
  <div class="work-detail">
    <div id="loader"></div>

    <!-- main-background -->
    <div
      class="main-detail-bg"
      :style="{
        'background-image':
          'url(../' + $page.portfolio.showcase.bg_img + ')',
      }"
    >
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
                <h2>{{ $page.portfolio.title }}</h2>
                <p class="project">
                  {{ $page.portfolio.tags }}
                </p>
                <div class="dash"></div>
                <p>
                  {{ $page.portfolio.short_description }}
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
              <h3>{{ $page.portfolio.title }}</h3>
              <p
                class="m-each"
                data-aos-once="true"
                data-aos="fade-up"
              >
                {{ $page.portfolio.long_description }}
              </p>

              <div
                class="image-work"
                data-aos-once="true"
                data-aos="fade-up"
                v-if="$page.portfolio.youtube !== 'null'"
              >
                <iframe
                  width="560"
                  height="315"
                  :src="$page.portfolio.youtube"
                  title="YouTube video player"
                  frameborder="0"
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                ></iframe>
              </div>

              <div
                data-aos-once="true"
                data-aos="fade-up"
                class="gallery-wrap"
              >
                <h3>Gallery</h3>
                <div class="image-container">
                  <g-link
                    :to="'../' + image.big_img"
                    target="_blank"
                    v-for="image in $page.portfolio.gallery.images"
                  >
                    <img
                      class="img-fluid"
                      :src="'../' + image.thumbnail"
                      alt="2"
                    />
                  </g-link>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Button Back -->
    <div class="btn-back">
      <g-link class="txt" to="/portfolio">Back to works </g-link>
      <span>
        <a href=""
          ><img src="../img/work-detail/back.png" alt="hh"
        /></a>
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
    title: 'hd',
  },
  mounted() {
    const custom = document.createElement('script');
    custom.setAttribute('src', '../../../js/custom.js');
    custom.async = true;
    document.head.appendChild(custom);

    console.log(this.$page.portfolio.gallery.images);
  },
};
</script>

<page-query>
    query Postfolio ($id: ID!) {
        portfolio: portfolio (id: $id) {
            title
            tags
            short_description
            long_description
            showcase{
                bg_img
            }
            youtube
            gallery{
                images{
                    thumbnail
                    big_img
                }
            }
        }
    }
  </page-query>

<style scoped lang="scss">
@import '../css/plugin.css';
@import '../css/style.css';
@import '../css/responsive.css';

.gallery-wrap {
  margin-top: 30px;
  .image-container {
    display: flex;
    flex-wrap: wrap;
    a {
      max-width: 50%;
      padding: 1em;

      &:hover{
        padding: 0;
      }
    }
  }
}
</style>
