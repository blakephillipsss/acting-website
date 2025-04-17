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
      <h1>Recently Seen In</h1>
      <FilmPosterComponent
        filmImage="silenced.jpg"
        filmTitle="Silenced (Click to watch on YouTube)"
        filmURL="https://www.youtube.com/watch?v=uiHkiUVnKL8&t=1s"
      />
      <FilmPosterComponent 
        filmImage="WOR.jpg" 
        filmTitle="When Olive Returned (Click to watch on YouTube)" 
        filmURL="https://www.youtube.com/watch?v=APAB9h2YjFw&t=4s"
      />
    </div>
    <div class="container-three" id="media-section">
      <h1>Demo Footage and Photos</h1>
      <!-- Main Demo Tape -->
      <VideoComponent youtubeEmbedUrl="https://www.youtube.com/embed/j_Mwf_5Li3k?si=rV16PEZumwtndrOx"/>
      <PhotoGalleryComponent/>
    </div>
    <div class="container-four" id="resume-section">
      <ResumeComponent pdfUrl="https://x4pg0p6fkhvy4kqt.public.blob.vercel-storage.com/Blake%20H.%20Phillips%20Mar%20%2725%20Resume-w7XXRTCPZp4wmmHQ47t2rrmLqsgLML.pdf"/>
    </div>
    <AttributionComponent/>
  </div>
    
</template>
  
<script>
  import ProfileComponent from './ProfileComponent.vue'
  import NavComponent from './NavComponent.vue'
  import SocialsComponent from './SocialsComponent.vue';
  import AboutMeComponent from './AboutMeComponent.vue'
  import FilmPosterComponent from './FilmPosterComponent.vue';
  import PhotoGalleryComponent from './PhotoGalleryComponent.vue';
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
      FilmPosterComponent,
      PhotoGalleryComponent,
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
    max-width: 30%;
    padding: 1%;
    margin: .5% 0.5% 2%;
  }

  .container-two {
    background-color: #F2F4FF;
    max-width: 34%;
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