<script setup>
import PrincipalView from '@/components/PrincipalView.vue';
import ChamadaView from './components/ChamadaView.vue';

</script>

<template>
  <div class="container">
    <div id="inicio">
      <PrincipalView />
    </div>
    <div id="rodape">
      <ChamadaView />
    </div>
  </div>

</template>

<style scoped>
  .container{
    display: flex;
    flex-direction: column;
    gap: 20px;
    padding: clamp(12px, 3vw, 16px);
    background-color: var(--color-branco);
  }
  #inicio{
    flex: 1;
  }
</style>
