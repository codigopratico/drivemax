<script setup>
import { ref } from 'vue'
import Review from './ReviewCard.vue';

const titulo = ref('O QUE NOSSOS CLIENTES DIZEM')

</script>

<template>
    <div class="main">
        <div class="titulo light">
            <h1>{{ titulo }}</h1>
        </div>
        <Review />
    </div>
</template>

<style scoped>
    .main{
        border-radius: 15px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 35px;
        padding-bottom: 35px;
        background-color: var(--bg-section-dark);
    }
    h1{
        color: var(--text-dark);
    }
</style>