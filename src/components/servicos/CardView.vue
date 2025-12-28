<script setup>
import { ref } from 'vue'

import necessidade from '@/assets/img/secao_2/icone_necessidade.png'
import busca from '@/assets/img/secao_2/icone_busca.png'
import negociacao from '@/assets/img/secao_2/icone_negociacao.png'

const servicos = ref([
    {id: 1, img: necessidade, alt: 'Necessidades', titulo: 'ANALISAMOS SUAS NECESSIDADES', subtitulo: 'Entendemos o que você procura.'},
    {id: 2, img: busca, alt: 'Avaliação', titulo: 'BUSCAMOS E AVALIAMOS OS MELHORES CARROS', subtitulo: 'Selecionamos as melhores opções para você.'},
    {id: 3, img: negociacao, alt: 'Negociação', titulo: 'NEGOCIAMOS O MELHOR PREÇO', subtitulo: 'Garantimos as melhores condições para a compra do seu carro.'}
    
])
</script>

<template>
    <div class="cards">
        <div 
        class="card"
        v-for="servico in servicos" 
        :key="servico.id"
        >
            <img 
            :src="servico.img" 
            :alt="servico.alt"
            >
            <div class="texto">
                <h2>{{ servico.titulo }}</h2>
                <p>{{ servico.subtitulo }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .cards{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        gap: 35px;
        padding: 0 10px;
    }.card{
        display: flex;
        flex-direction: column;
        padding: 15px 10px;
        gap: 10px;
        align-items: center;
        height: 350px;
        flex: 1 1 260px;
        max-width: 300px;
        text-align: center;
        box-shadow: 10px 4px 20px rgba(0, 0, 0, 0.2);
        background-color: var(--color-branco);
        border-radius: 15px;
        transition: ease-in-out 300ms;
    }.card:hover{
        transform: scale(1.01);
        box-shadow: 10px 4px 20px rgba(0, 0, 0, 0.5);
    }
    .texto{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 25px;
        width: 100%;
    }
    h2, p{
        color: var(--color-preto-texto);
    }
    h2{
        font-size: var(--text-servicos-titulo);
    }
    p{
        font-size: var(--text-servicos-subtitulo);
    }
    img{
        width: fit-content;
        height: 140px;
    }
</style>