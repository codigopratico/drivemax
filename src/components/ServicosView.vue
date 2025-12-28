<script setup>
import { ref } from 'vue'
import CardView from './servicos/CardView.vue';

const titulo = ref('COMO A DRIVEMAX PODE AJUDAR VOCÊ')
const btn = ref('FALE COM UM CONSULTOR')
</script>

<template>
    <div class="servicos">
        <div class="titulo">
            <h1>{{ titulo }}</h1>
        </div>
        <CardView />
        <div class="botao">
            <button>{{ btn }}</button>
        </div>
    </div>
</template>

<style scoped>
    .servicos{
        background-color: var(--color-fundo-branco);
        border-radius: 15px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 80px;
        padding: 0 0 25px 0;
    }
    .botao button{
        font-size: var(--text-butao-responsivo);
        text-shadow: 10px 10px 25px #fff;
    }


    @media screen and (max-width: 768px) {
        .servicos{
            gap: 35px;
        }
    }
</style>