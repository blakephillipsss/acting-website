<template>
  <div class="gallery-images">
    <LightGallery 
      :settings="{ speed: 500, plugins: plugins }" 
      @onInit="onInit" 
      @onBeforeSlide="onBeforeSlide"
      >
      <a v-for="(img, index) in galleryImages" :key="index" :href="img">
        <img :src="img" alt="<i>Silenced</i>, Dir. Brittney Van Mil" class="gallery-image" />
      </a>
    </LightGallery>
  </div>
</template>

<script>
  import LightGallery from 'lightgallery/vue';
  import lgThumbnail from 'lightgallery/plugins/thumbnail';
  import lgZoom from 'lightgallery/plugins/zoom';

  import 'lightgallery/scss/lightgallery.scss';

  export default {
    name: 'PhotoGalleryComponent',
    components: {
      LightGallery,
    },
    data() {
      return {
        plugins: [lgThumbnail, lgZoom],
        galleryImages: []
      };
    },
    created() {
      const imagesContext = require.context('../assets/galleryPics', false, /\.(png|jpe?g|svg)$/);
      this.galleryImages = imagesContext.keys().map(imagesContext);
    },
    methods: {
      onInit() {
        console.log('LightGallery has been initialized');
      },
      onBeforeSlide() {
        console.log('calling before slide');
      }
    }
  }
</script>
<style lang="scss" scoped>
  @import 'lightgallery/css/lightgallery.css';
  @import 'lightgallery/css/lg-thumbnail.css';
  @import 'lightgallery/css/lg-zoom.css';
  .gallery-images {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
  .gallery-images img {
    display: block;
    padding: 1rem;
    width: 95%;
    object-fit: cover;
  }
  .gallery-images a {
    display: flex;
    justify-content: center;
  }
</style>
