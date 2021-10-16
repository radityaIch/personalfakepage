<template>
  <NavigationComponent />
  <WelcomeMessage />
  <AboutMe id="about"/>
  <div class="separator mb-5" id="projects"></div>
  <MyProjects />
  <div class="separator mb-5" id="socials"></div>
  <Socials />
  <div class="separator mb-5" style="margin-bottom: 10vh"></div>
  <ModalExample />
</template>
<style>
  html {
    scroll-behavior: smooth;
  }
</style>
<script>
import NavigationComponent from './components/NavigationComponent.vue'
import WelcomeMessage from './components/LandingPage/WelcomeMessage.vue'
import AboutMe from './components/LandingPage/AboutMe.vue'
import MyProjects from './components/LandingPage/MyProjects.vue'
import Socials from './components/LandingPage/Socials.vue'
import ModalExample from './components/ModalExample.vue'

export default {
  name: 'App',
  components: {
    NavigationComponent,
    WelcomeMessage,
    AboutMe,
    MyProjects,
    Socials,
    ModalExample
  },
  created(){
    document.title = 'Ichinomiya Mori Personal Page'
  }
}
</script>