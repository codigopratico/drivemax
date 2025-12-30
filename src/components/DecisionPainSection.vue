<script setup>
import { ref } from 'vue'

import UiCard from './UiCard.vue';
import opcoes from '@/assets/img/secao_1/icone_opcoes.png'
import medo from '@/assets/img/secao_1/icone_medo.png'
import dificuldade from '@/assets/img/secao_1/icone_dificuldade.png'

const servicos = ref([
    {
        id: 1, 
        img: opcoes, 
        alt: 'Opções', 
        titulo: 'MUITAS OPÇÕES?', 
        subtitulo: 'Está perdido com tantas oportunidades?'
        },
        {
            id: 2,
            img: medo,
            alt: 'Medo',
            titulo: 'MEDO DE SER ENGANADO?',
            subtitulo: 'Preocupado com fraudes ou golpes?'
        },
        {
            id: 3,
            img: dificuldade,
            alt: 'Dificuldade',
            titulo: 'NÃO ENTENDE DE VEÍCULOS?',
            subtitulo: 'Não sabe avaliar um carro usado?'
        }
])

const titulo = ref('DIFICULDADE PARA ESCOLHER O CARRO IDEAL?')
const subtitulo = ref('Nós estamos aqui para ajudar você.')

</script>

<template>
    <div class="main">
        <div class="titulo light">
            <h1>{{ titulo }}</h1>
        </div>
        <div class="conteudo">
            <UiCard :servicos="servicos" />
            <hr>
            <h2>{{ subtitulo }}</h2>
        </div>
    </div>
</template>

<style scoped>
    .main{
        display: flex;
        flex-direction: column;
        gap: 35px;
        background-color: var(--bg-section-dark);
        padding: 0 0 25px 0;
        border-radius: 15px;
    }
    .conteudo{
        display: flex;
        flex-direction: column;
        gap: 35px;
        align-items: center;
    }
    h1{
        color: var(--text-dark);
    }
    hr{
        width: 90%;
        border: 1px solid var(--border-default);
    }
    h2{
        color: var(--text-primary);
        font-size: var(--font-title-sm);
        text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
    }

</style>