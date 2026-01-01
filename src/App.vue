<script setup>
import { onMounted } from 'vue'

import Home from '@/components/HomeView.vue';
import ChamadaView from './components/ContactSection.vue';
import Services from './components/ServicesSection.vue';
import Security from './components/SecuritySection.vue';
import Decision from './components/DecisionPainSection.vue';
import Review from './components/ReviewSection.vue';

onMounted(() => {
  const sections = document.querySelectorAll('section')

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if(entry.isIntersecting){
        entry.target.classList.add('visible')
        observer.unobserve(entry.target)
      }
    })
  })
  sections.forEach(section => observer.observe(section))
})

</script>

<template>
  <div class="container">
    <div class="blur">

    </div>
    <section id="home">
      <Home />
    </section>

    <section id="services">
      <Services />
    </section>

    <section id="review">
      <Review />
    </section>

    <section id="security">
      <Security />
    </section>

    <section class="decision">
      <Decision />
    </section>

    <section id="contact">
      <ChamadaView />
    </section>
  </div>

</template>

<style scoped>
  .container{
    display: flex;
    flex-direction: column;
    gap: 25px;
    padding: clamp(12px, 3vw, 16px);
    background-color: var(--bg-page-light);
  }
  #inicio{
    flex: 1;
  }
  section{
    border: 1px solid var(--border-default);
    border-radius: 15px;
    box-shadow: 5px 5px 15px rgba(0, 0, 0, .3);
    opacity: 0;
    transform: translateY(0);
    transition: opacity 1.3s ease-out, transform 1.3s ease-out;
  }
  section.visible{
    opacity: 1;
    transform: translateY(5px);
  }
  .blur{
    background-color: rgba(0, 0, 0, .8);
    position: fixed;
    bottom: 0;
    height: 3%;
    width: 100%;
    filter: blur(25px);
    z-index: 100;
  }
</style>
