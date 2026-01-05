<template>
  <div id="app">
    <NavBar />
    <Hero />
    <Classes />
    <Trainers />
    <Pricing />
    <Contact />
    <Footer />
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import Hero from './components/Hero.vue'
import Classes from './components/Classes.vue'
import Trainers from './components/Trainers.vue'
import Pricing from './components/Pricing.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<style scoped>
#app {
  position: relative;
}
</style>

