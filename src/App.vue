<script setup lang="ts">
import Navigation from './components/Navigation.vue'
import Home from './views/Home.vue'
import Projects from './views/Projects.vue'
import About from './views/About.vue'
import Contact from './views/Contact.vue'
</script>

<template>
  <Navigation />
  <div class="snap-y snap-mandatory">
    <section id="home" class="snap-start">
      <Home />
    </section>
    <section id="projects" class="snap-start">
      <Projects />
    </section>
    <section id="about" class="snap-start">
      <About />
    </section>
    <section id="contact" class="snap-start">
      <Contact />
    </section>
  </div>
</template>

<style>
html {
  scroll-behavior: smooth;
}
</style>