<!-- MainPage.vue -->
<template>
    <div class="main-container">
        <div class="container-one">
            <ProfileComponent/>
            <NavComponent @scroll-to="scrollTo" />

            <!-- <SocialLinks /> -->
        </div>

        <!-- <AboutMe />

        <RecentProjects />

        <DemoSection :youtube-embed-url="youtubeEmbedUrl" />

        <ResumeSection :pdf-url="pdfUrl" /> -->
    </div>
</template>
  
<script>
    // import { ref, onMounted, onBeforeUnmount } from 'vue'
    import ProfileComponent from './ProfileComponent.vue'
    import NavComponent from './NavComponent.vue'
    // import SocialLinks from './components/SocialLinks.vue'
    // import AboutMe from './components/AboutMe.vue'
    // import RecentProjects from './components/RecentProjects.vue'
    // import DemoSection from './components/DemoSection.vue'
    // import ResumeSection from './components/ResumeSection.vue'
    
    export default {
        name: 'MainPage',
        components: {
            ProfileComponent,
            NavComponent//,
        // SocialLinks,
        // AboutMe,
        // RecentProjects,
        // DemoSection,
        // ResumeSection
        }//,
        // setup() {
        // const pdfUrl = ref('https://x4pg0p6fkhvy4kqt.public.blob.vercel-storage.com/Blake%20H.%20Phillips%20Resume-DNDlhAd7cSMZ6Q31IVzXjDLzVjt622.pdf')
        // const youtubeEmbedUrl = ref('https://www.youtube.com/embed/wIjbAvhwO1k?si=XfR5-tNOVJi8AJcd')
    
        // const scrollTo = (elementId) => {
        //     const element = document.getElementById(elementId)
        //     if (element) {
        //     element.scrollIntoView({ behavior: 'smooth' })
        //     }
        // }
    
        // onMounted(() => {
        //     // Fade-in animation logic
        // })
    
        // return {
        //     pdfUrl,
        //     youtubeEmbedUrl,
        //     scrollTo
        // }
        // }
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
  min-width: 350px;
  margin: 10px;
  border-radius: 25px;
  /* opacity: 0; */
  transform: translateY(20px);
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

/* About Me Styles */
.about-me h1 {
  text-align: center;
}

.about-me p {
  text-align: justify;
  margin: 2%;
}

/* Films Styles */
.films {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}

.films a {
  text-align: center;
  margin: 1rem;
  text-decoration: underline;
  color: #2c3e50;
  transition: transform 0.3s ease;
}

.films a:hover {
  transform: scale(1.05);
}

.films img {
  height: 20rem;
  padding: 1rem;
  display: block;
  margin: 0 auto;
}

/* Social Media Styles */
.socials {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

.socials a {
  margin-top: 3%;
  padding: .5%;
  transition: transform 0.3s ease;
}

.socials a:hover {
  transform: scale(1.1);
}

.socials img {
  height: 2.75rem;
}

/* Video Styles */
.video-wrapper {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 aspect ratio */
  height: 0;
  overflow: hidden;
  width: 100%;
}

.video-wrapper iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

/* Resume Styles */
.container-four h1 {
  color: #f2f4ff;
}

/* PDF Styles */
.pdf-wrapper {
  width: 100%;
  height: 0;
  padding-bottom: 129.4%; /* Aspect ratio for A4 paper */
  position: relative;
  overflow: hidden;
}
.pdf-wrapper object {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
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