<template>
  <div>
    <Navbar />

    <main>
      <Hero />
      <About />
      <Projects />
      <Contact />
      <Footer />
    </main>

 
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
main {
  padding: 20px;
}
</style>
