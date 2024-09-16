<template>
  <div class="button-container">
    <div class="nav-button">
      <a href="#media-section" @click.prevent="scrollTo('media-section')">Demo Footage and Photos</a>
    </div>
    <div class="nav-button">
      <a href="#resume-section" @click.prevent="scrollTo('resume-section')">Resume</a>
    </div>
  </div>
</template>

<script setup>
  const scrollTo = (elementId) => {
    const element = document.getElementById(elementId)
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' })
    }
  }
</script>
  
<style scoped>
/* Button Styles */
.button-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.nav-button {
  background-color: #595758;
  margin: 2%;
  padding: 12px;
  border-radius: 15px;
  width: 100%;
  transition: background-color 0.3s ease;
}

.nav-button:hover {
  background-color: #7a7879;
}

.nav-button a {
  text-decoration: none;
  color: #f2f4ff;
}
</style>