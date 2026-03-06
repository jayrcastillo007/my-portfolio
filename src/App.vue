
<template>
  <div class="min-h-screen bg-slate-950 text-white">
    <Navbar />
    <Hero />
    <main class="mx-auto w-full max-w-7xl px-6 lg:px-7">
      <About />
      <Skills />
      <Projects />
      <Contact />
    </main>
    <!-- <Footer /> -->
  </div>
</template>

<script setup>
import Navbar from "./components/Navbar.vue"
import Hero from "./components/Hero.vue"
import About from "./components/About.vue"
import Skills from "./components/Skills.vue"
import Projects from "./components/Projects.vue"
import Contact from "./components/Contact.vue"
// import Footer from "./components/Footer.vue"
</script>