<template>
  <div class="gallery-images">
    <LightGallery 
      :settings="{ speed: 500, plugins: plugins }" 
      @onInit="onInit" 
      @onBeforeSlide="onBeforeSlide"
      >
      <a v-for="(img, index) in galleryImages" :key="index" :href="img">
        <img :src="img" alt="Gallery image" class="gallery-image" />
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
    .gallery-images img {
  height: 20rem;
  padding: 1rem;
  display: block;
  margin: 0 auto;
}
</style>
