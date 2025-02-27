<template>
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
        </ul>
      </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
const showAttributions = ref(false)

const toggleAttributions = () => {
  showAttributions.value = !showAttributions.value
}
</script>

<style scoped>
    .attributions-section {
  width: 100%;
  padding: 10px;
  background-color: #96C5F7;
  color: #595758;
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
  color: #595758;
  text-decoration: none;
}

.attribution-content a:hover {
  text-decoration: underline;
}
</style>