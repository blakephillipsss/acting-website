<!-- MainPage.vue -->
<template>
  <div class="main-container">
    <div class="container-one">
      <ProfileComponent/>
      <NavComponent @scroll-to="scrollTo" />
      <SocialsComponent/>
    </div>
    <div class="container-two">
      <AboutMeComponent />
      <h1>Clips from Class</h1>
      <h3>From scene study with John Gordon at The Dirt Underneath</h3>
      <p>Want to see footage from my recent unreleased work? Shoot me a message <a :href="'mailto:acting@blakehphillips.com'">here</a> and I'll send you a private link!</p>
      <!-- Main Demo Tape -->
      <VideoComponent youtubeEmbedUrl="https://www.youtube.com/embed/wznk4hxcT6M?si=JAXHvhD9QgFKfdD5"/>
      <VideoComponent youtubeEmbedUrl="https://www.youtube.com/embed/mD1yOIPnbdw?si=YOgia9xEQUPS7d5T"/>
      <VideoComponent youtubeEmbedUrl="https://www.youtube.com/embed/Ugamf5roUOk?si=9afBVQBuerjWa1H1"/>
      <VideoComponent youtubeEmbedUrl="https://www.youtube.com/embed/SvnM6_b_Czs?si=jvHV48HLRq15seqc"/>
      <!-- <br> -->
      <!-- <PhotoGalleryComponent/> -->
    </div>
    <div class="container-four" id="resume-section">
      <ResumeComponent pdfUrl="https://x4pg0p6fkhvy4kqt.public.blob.vercel-storage.com/20260213_Blake_H_Phillips_Resume.pdf"/>
    </div>
    <AttributionComponent/>
  </div>
    
</template>
  
<script>
  import ProfileComponent from './ProfileComponent.vue'
  import NavComponent from './NavComponent.vue'
  import SocialsComponent from './SocialsComponent.vue';
  import AboutMeComponent from './AboutMeComponent.vue'
  // import FilmPosterComponent from './FilmPosterComponent.vue';
  // import PhotoGalleryComponent from './PhotoGalleryComponent.vue';
  import VideoComponent from './VideoComponent.vue';
  import ResumeComponent from './ResumeComponent.vue'
  import AttributionComponent from './AttributionComponent.vue';
  
  export default {
    name: 'MainPage',
    components: {
      ProfileComponent,
      NavComponent,
      SocialsComponent,
      AboutMeComponent,
      // FilmPosterComponent,
      // PhotoGalleryComponent,
      VideoComponent,
      ResumeComponent,
      AttributionComponent
    }
  }
</script>

<style scoped>
  /* Global Styles */
  .main-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
    background-color: #96C5F7;
    border-radius: 25px;
    width: 100%;
  }

  /* Container Styles */
  .container-one, .container-two, .container-three, .container-four {
    flex: 1;
    min-width: 309px;
    margin: 10px;
    border-radius: 25px;
    /* opacity: 0; */
    /* transform: translateY(20px); */
  }

  .container-one {
    background-color: #304C89;
    /* max-width: 30%; */
    padding: 1%;
    margin: .5% 0.5% 2%;
  }

  .container-two {
    background-color: #F2F4FF;
    /* max-width: 34%; */
    margin: 0.5%;
  }

  .container-three, .container-four {
    width: 36%;
    margin: 0.5%;
  }

  .container-three {
    background-color: #F2F4FF;
  }

  .container-four {
    background-color: #304C89;
  }

  /* Animation Styles */
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .fade-in {
    animation: fadeIn 0.5s ease-out forwards;
  }

/* Responsive Styles */
  @media (max-width: 768px) {
    .container-one, .container-two, .container-three, .container-four {
      max-width: 100%;
      width: 100%;
    }
    .video-wrapper, .pdf-wrapper {
      width: 100%;
    }
  }

</style>