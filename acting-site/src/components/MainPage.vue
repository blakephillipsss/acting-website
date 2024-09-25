<!--HTML code-->
<!-- To-do: -->
<!-- - Update favicon to something better -->
<!-- - move assets to public folder -->
<!-- - break up main page into components -->
<!-- - write an actual about me -->
<template>
    <head><title>Blake H. Phillips</title></head>
    <div class="main-container">
        <div class="container-one">
            <div class="profile">
                <h1>Blake H. Phillips</h1>
                <p>(he/him/his)</p>
                <img src="../assets/Blake H. Phillips Headshot.jpg" alt="" class="">
                <p>Non-Union Toronto Actor</p>
                <a href="mailto:acting@blakehphillips.com">acting@blakehphillips.com</a>
                <p>+1 (416) 818-1156</p>
            </div>
            <div class="button-container">
                <div class="demos-button">
                    <a href="#demo-section" @click.prevent="scrollTo('demo-section')">Demo Footage and Media</a>
                </div>
                <div class="demos-button">
                    <a href="#resume-section" @click.prevent="scrollTo('resume-section')">Resume</a>
                </div>
            </div>
            <div class="external-links">
                <div class="socials">
                    <a href="https://www.imdb.com/name/nm16436371/?ref_=ttfc_fc_cl_t11">
                        <img src="../assets/imdb.png" alt="">
                    </a>
                    <a href="https://www.instagram.com/blakehphillips/" target="_blank" rel="noopener noreferrer">
                        <img src="../assets/instagram.png" alt="">
                    </a>
                    <a href="https://www.youtube.com/@blakehphillips" target="_blank" rel="noopener noreferrer">
                        <img src="../assets/youtube.png" alt="">
                    </a>
                    <a href="https://www.linkedin.com/in/bhp42/" target="_blank" rel="noopener noreferrer">
                        <img src="../assets/linkedin.png" alt="">
                    </a>
                </div>
            </div>
            
        </div>
        <div class="container-two">
            <div class="about-me">
                <h1>About Blake</h1>
                <p>Blake H. Phillips is an emerging actor out of Toronto, Canada. With a dedication to his craft, Blake is rapidly making a name for himself as a versatile actor capable of delivering powerful, natural performances on camera. 
                    Join Blake on his exciting journey as he continues to rise throughout his acting career.</p>
            </div>
            <div class="recent-projects">
                <h1>Recently Seen In</h1>
                <div class="films">
                    <a href="https://youtu.be/APAB9h2YjFw?si=E2WHXnkXmlt8BXTa">
                        <img src="../assets/WOR.jpg" alt="">
                        <p><b>When Olive Returned (Watch Now!)</b></p>
                    </a>
                    <a href="">
                        <img src="../assets/oh_sadie.jpg" alt="">
                        <p><b>Oh, Sadie! (Coming Soon!)</b></p>
                    </a>
                </div>
            </div>
        </div>
        <div id="demo-section" class="container-three">
            <div class="youtube-video">
                <h1>Demo and Media</h1>
                <!-- Embed YouTube Videos -->
                <div class="video-wrapper">
                    <iframe :src="youtubeEmbedUrl" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </div>
            </div>
        </div>
        <div id="resume-section" class="container-four">
            <div class="pdfs">
                <h1>Resume</h1>
                <div class="pdf-wrapper">
                    <object :data="pdfUrl" type="application/pdf" width="100%" height="500px">
                        <p>Unable to display PDF file. <a :href="pdfUrl">Download</a> instead.</p>
                    </object>
                </div>
            </div>
        </div>
        <div class="attributions-section">
      <button @click="toggleAttributions" class="attribution-toggle">
        {{ showAttributions ? 'Hide Attributions' : 'Show Attributions' }}
      </button>
      <div v-if="showAttributions" class="attribution-content">
        <h3>Attributions</h3>
        <ul>
          <li>Fonts: Bodoni MT Condensed</li>
          <li><a href="https://www.flaticon.com/free-icons/instagram" title="instagram icons" target="_blank" rel="noopener noreferrer">Instagram icons created by Freepik - Flaticon</a></li>
          <li><a href="https://www.flaticon.com/free-icons/youtube" title="youtube icons" target="_blank" rel="noopener noreferrer">Youtube icons created by Freepik - Flaticon</a></li>
          <li><a href="https://www.flaticon.com/free-icons/linkedin" title="linkedin icons" target="_blank" rel="noopener noreferrer">Linkedin icons created by Freepik - Flaticon</a></li>
          <li><a href="https://www.flaticon.com/free-icons/imdb" title="imdb icons" target="_blank" rel="noopener noreferrer">Imdb icons created by Freepik - Flaticon</a></li>
          <!-- Add more attribution items as needed -->
        </ul>
      </div>
    </div>
    </div>
</template>

<!--JS code-->
<script setup>
import { ref, onMounted, onBeforeUnmount, nextTick } from 'vue'

const pdfUrl = ref("https://x4pg0p6fkhvy4kqt.public.blob.vercel-storage.com/Blake%20H.%20Phillips%20Aug%20'24%20Resume-nUVBzuokngQFzQbn1swu6y31A48tZa.pdf")
const youtubeEmbedUrl = ref('https://www.youtube.com/embed/j_Mwf_5Li3k?si=rV16PEZumwtndrOx')

const scrollTo = (elementId) => {
  const element = document.getElementById(elementId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}

const updatePdfZoom = () => {
  const pdfObject = document.querySelector('.pdf-wrapper object')
  if (pdfObject) {
    pdfObject.style.zoom = '100%'
    pdfObject.style.height = `${pdfObject.offsetWidth * 1.3}px` // Adjust this multiplier as needed
  }
}

const handleResize = () => {
  updatePdfZoom()
}

onMounted(() => {
  nextTick(() => {
    document.querySelectorAll('.container-one, .container-two, .container-three, .container-four').forEach((el, index) => {
      setTimeout(() => {
        el.classList.add('fade-in')
      }, index * 200)
    })
    updatePdfZoom()
    window.addEventListener('resize', handleResize)
  })
})

onBeforeUnmount(() => {
  window.removeEventListener('resize', handleResize)
})

const showAttributions = ref(false)

const toggleAttributions = () => {
  showAttributions.value = !showAttributions.value
}
</script>

<!--CSS code-->
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
  opacity: 0;
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

/* Profile Styles */
.profile h1 {
  color: #f2f4ff;
  font-family: "Bodoni MT Condensed", serif;
  font-size: 2.8rem;
}

.profile img {
  height: auto;
  max-width: 100%;
}

.profile p, .profile a {
  color: #f2f4ff;
}

.profile p {
  font-size: 1.2rem;
}

.profile a {
  text-decoration: underline;
}

/* Button Styles */
.button-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.demos-button {
  background-color: #595758;
  margin: 2%;
  padding: 12px;
  border-radius: 15px;
  width: 100%;
  transition: background-color 0.3s ease;
}

.demos-button:hover {
  background-color: #7a7879;
}

.demos-button a {
  text-decoration: none;
  color: #f2f4ff;
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

.pdf-wrapper p, a{
    color: #f2f4ff;
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

/* Attributions Section Styles */
.attributions-section {
  width: 100%;
  padding: 10px;
  background-color: #304C89;
  color: #f2f4ff;
  font-size: 0.9rem;
  text-align: center;
  margin-top: 20px;
  border-radius: 0 0 25px 25px;
}

.attribution-toggle {
  background-color: #595758;
  color: #f2f4ff;
  border: none;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.attribution-toggle:hover {
  background-color: #7a7879;
}

.attribution-content {
  margin-top: 10px;
}

.attribution-content h3 {
  font-size: 1.1rem;
  margin-bottom: 5px;
}

.attribution-content ul {
  list-style-type: none;
  padding: 0;
}

.attribution-content li {
  margin-bottom: 5px;
}

.attribution-content a {
  color: #96C5F7;
  text-decoration: none;
}

.attribution-content a:hover {
  text-decoration: underline;
}
</style>