<script setup>
import Home from '@/components/HomeView.vue';
import ChamadaView from './components/ContactSection.vue';
import Services from './components/ServicesSection.vue';
import Security from './components/SecuritySection.vue';
import Decision from './components/DecisionPainSection.vue';
import Review from './components/ReviewSection.vue';


</script>

<template>
  <div class="container">
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
  }
</style>
