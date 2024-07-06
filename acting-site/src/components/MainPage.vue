<!--HTML code-->
<template>
    <head><title>Blake H. Phillips</title></head>
    <div class="main-container">
        <div class="container-one">
            <div class="profile">
                <h1>Blake H. Phillips</h1>
                <img src="../assets/Blake H. Phillips Headshot.jpg" alt="" class="">
                <p>Non-Union Toronto Actor</p>
                <a href="mailto:acting@blakehphillips.com">acting@blakehphillips.com</a>
                <p>+1 (416) 818-1158</p>
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
                    <a href="">
                        <img src="../assets/imdb.png" alt="">
                    </a>
                    <a href="https://www.instagram.com/blakehphillips/">
                        <img src="../assets/ig.png" alt="">
                    </a>
                    <a href="https://www.youtube.com/@blakehphillips">
                        <img src="../assets/yt.png" alt="">
                    </a>
                    <a href="https://www.linkedin.com/in/bhp42/">
                        <img src="../assets/li.png" alt="">
                    </a>
                </div>
            </div>
            
        </div>
        <div class="container-two">
            <div class="about-me">
                <h1>About Blake</h1>
                <p>Blake H. Phillips is an emerging talent in the world of acting and writing, driven by a passion for storytelling and a commitment to exploring the human condition. With a dedication to his craft, Blake is rapidly making a name for himself as a versatile actor capable of delivering powerful performances across a range of genres. 
                    Join Blake on his exciting journey as he strives to make his mark as both an actor and a writer, sharing incredible stories with the world.</p>
            </div>
            <div class="recent-projects">
                <h1>Recently Seen In</h1>
                <div class="films">
                    <a href="">
                        <img src="../assets/WOR.jpg" alt="">
                        <p><b>When Olive Returned (Coming Soon!)</b></p>
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
                <iframe width="560" height="315" src="https://www.youtube.com/embed/wIjbAvhwO1k?si=XfR5-tNOVJi8AJcd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
        <div id="resume-section" class="container-four">
            <div class="pdfs">
                <h1>Resume</h1>
                <object :data="pdfUrl" type="application/pdf" width="100%" height="500px">
                    <p>Unable to display PDF file. <a :href="pdfUrl">Download</a> instead.</p>
                </object>
            </div>
        </div>
    </div>
</template>

<!--JS code-->
<script>
export default {
    data() {
        return {
            pdfUrl: 'https://x4pg0p6fkhvy4kqt.public.blob.vercel-storage.com/Blake%20H.%20Phillips%20Resume-DNDlhAd7cSMZ6Q31IVzXjDLzVjt622.pdf'
        }
  },
  methods: {
    scrollTo(elementId) {
      const element = document.getElementById(elementId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    }
  },
  mounted() {
    // Add animation classes after component is mounted
    this.$nextTick(() => {
      document.querySelectorAll('.container-one, .container-two, .container-three, .container-four').forEach((el, index) => {
        setTimeout(() => {
          el.classList.add('fade-in');
        }, index * 200);
      });
    });
  }
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
  }
}
</style>