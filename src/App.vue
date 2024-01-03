<template>
  <NavBar/>
  <AboutHero/>
  <HeroSection/>
  <ServiceSection/>
</template>

<script>
import NavBar from './components/NavBar.vue'
import AboutHero from './components/AboutHero.vue'
import HeroSection from './components/HeroSection.vue'
import ServiceSection from './components/Service-Section.vue'

export default {
  name: 'App',
  components: {
    NavBar, AboutHero, HeroSection, ServiceSection
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400&display=swap");
:root {
  --font-inter: Inter;
  --font-size-5xl: 24px;
  --color-white: #fff;
}

*{
  margin: 0px;
  padding: 0px;
}
#app {
  line-height: normal;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
