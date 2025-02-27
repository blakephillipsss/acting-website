<template>
    <div class="resume-section">
        <h1>Resume</h1>
        <div class="pdf-wrapper">
            <object :data="pdfUrl" type="application/pdf" width="100%" height="500px">
                <p>Unable to display PDF file. <a :href="pdfUrl">Download</a> instead.</p>
            </object>
        </div>
    </div>
        
</template>

<script setup>
/* eslint-env vue/setup-compiler-macros */
import { onMounted, nextTick, onBeforeUnmount, toRefs } from 'vue';

const props = defineProps({
  pdfUrl: {
    type: String,
    default: "Unable to display PDF file. Please contact me for a copy."
  }
});

const { pdfUrl } = toRefs(props);

const updatePdfZoom = () => {
  const pdfObject = document.querySelector('.pdf-wrapper object');
  if (pdfObject) {
    pdfObject.style.zoom = '100%';
    pdfObject.style.height = `${pdfObject.offsetWidth * 1.3}px`;
  }
};

const handleResize = () => {
  updatePdfZoom();
};

onMounted(() => {
  nextTick(() => {
    // Apply fade-in animation to containers on the main page
    document.querySelectorAll('.container-one, .container-two, .container-three, .container-four')
      .forEach((el, index) => {
        setTimeout(() => {
          el.classList.add('fade-in');
        }, index * 200);
      });
    updatePdfZoom();
    window.addEventListener('resize', handleResize);
  });
});

onBeforeUnmount(() => {
  window.removeEventListener('resize', handleResize);
});
</script>

<style scoped>
.resume-section h1, p {
  color: #f2f4ff;
}

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
</style>