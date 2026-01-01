<script setup>
import { ref } from 'vue'
import UiCard from './UiCard.vue';

import necessidade from '@/assets/img/secao_2/icone_necessidade.png'
import busca from '@/assets/img/secao_2/icone_busca.png'
import negociacao from '@/assets/img/secao_2/icone_negociacao.png'

const servicos = ref([
    {
        id: 1, 
        img: necessidade, 
        alt: 'Necessidades', 
        titulo: 'ANALISAMOS SUAS NECESSIDADES', 
        subtitulo: 'Entendemos o que você procura.'
    },
    {
        id: 2, 
        img: busca, 
        alt: 'Avaliação', 
        titulo: 'BUSCAMOS E AVALIAMOS OS MELHORES CARROS', 
        subtitulo: 'Selecionamos as melhores opções para você.'
    },
    {
        id: 3, 
        img: negociacao, 
        alt: 'Negociação', 
        titulo: 'NEGOCIAMOS O MELHOR PREÇO', 
        subtitulo: 'Garantimos as melhores condições para a compra do seu carro.'
    }
    
])

const titulo = ref('COMO A DRIVEMAX PODE AJUDAR VOCÊ')
const btn = ref('FALE COM CONSULTOR')
</script>

<template>
    <div class="servicos">
        <div class="titulo">
            <h1>{{ titulo }}</h1>
        </div>
        <UiCard :servicos="servicos" />
        <div class="botao">
            <button><a href="https://github.com/codigopratico" target="_blank">{{ btn }}</a></button>
        </div>
    </div>
</template>

<style scoped>
    .servicos{
        background-color: var(--bg-section-light);
        border-radius: 15px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 80px;
        padding: 0 0 25px 0;
    }
    .botao button{
        font-size: var(--font-button-xl);
        text-shadow: 10px 10px 25px #fff;
        border: 1px solid var(--text-dark);
    }
    button a{
        padding: 10px;
    }


    @media screen and (max-width: 768px) {
        .servicos{
            gap: 35px;
        }
    }
</style>