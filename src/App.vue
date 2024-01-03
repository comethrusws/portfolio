<template>
  <NavBar/>
  <AboutHero/>
  <HeroSection/>
  <ServiceSection/>
  <ContactSection/>

  <FooterBar/>
</template>

<script>
import NavBar from './components/NavBar.vue'
import AboutHero from './components/AboutHero.vue'
import HeroSection from './components/HeroSection.vue'
import ServiceSection from './components/Service-Section.vue'
import FooterBar from './components/FooterBar.vue'
import ContactSection from './components/ContactSection.vue'

export default {
  name: 'App',
  components: {
    NavBar, AboutHero, HeroSection, ServiceSection, FooterBar, ContactSection
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400&display=swap");
*{
  margin: 0px;
  padding: 0px;
}
#app {
  line-height: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
