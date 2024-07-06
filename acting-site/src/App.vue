<template>
  <MainPage/>
  <SpeedInsights />
</template>

<script>
import MainPage from './components/MainPage.vue';
import { SpeedInsights } from "@vercel/speed-insights/vue"

export default {
  name: 'App',
  components: {
    MainPage,
    SpeedInsights
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
