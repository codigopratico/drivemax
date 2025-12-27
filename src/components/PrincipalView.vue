<script setup>
import { ref } from 'vue'

import CabecalhoView from '@/components/home/CabecalhoView.vue'

const texto = ref('Nós ajudamos você a comprar o carro ideal com segurança e confiança.')

const btn1 = ref('AGENDAR CONSULTORIA')
const btn2 = ref('Saiba Mais')
</script>

<template>
    <div class="main">
        <CabecalhoView />
        <div class="conteudo">
            <h1>ESCOLHER O <span>CARRO CERTO</span> PODE SER COMPLICADO.</h1>
            <h4>{{ texto }}</h4>
            <div class="botoes">
                <button>{{ btn1 }}</button>
                <button id="secundario">{{ btn2 }}</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
    /* Imagem de Funco */
    .main{
        background-color: var(--color-preto);
        height: 100vh;
        width: 100%;
        position: relative;
        z-index: 1;
        border-radius: 15px;
    }

    .main::before{
        content: "";
        background-image: url('/src/assets/img/home/pagina_home.png');
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center top;
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        opacity: 0.7;
        z-index: -1;
        border-radius: 15px;
    }

    @media screen and (max-width: 500px) {
        .main::before{
            background-position: 68% top;
        }
    }

    /* Conteúdo */
    .conteudo{
        padding: 190px 0 0 3%;
        display: flex;
        flex-direction: column;
        width: 100%;
        height: 100%;
        gap: 40px;
    }.conteudo h1{
        font-size: var(--text-titulo);
        text-shadow: 10px 10px 100px #1f1f1f;
        width: 65%;
    }.conteudo h4{
        font-size: var(--text-subtitulo);
        width: 40%;
        text-shadow: 10px 10px 100px #1f1f1f;
    }
    button#secundario{
        background-color: var(--color-texto-secundario);
        border: 1px solid var(--color-branco);
        padding: 10px;
    }
    span{
        color: var(--color-laranja);
    }

    .botoes{
        display: flex;
        gap: 10px;
    }.botoes button{
        font-size: var(--text-butao-principal);
    }

    @media screen and (max-width: 1024px){
        .conteudo{
            padding: 160px 0 0 3%;
        }
        .conteudo h4{
            width: 50%;
        }
    }

    @media screen and (max-width: 920px){
        .conteudo h1{
            width: 85%;
        }
        .conteudo h4{
            width: 65%;
        }
    }

    @media screen and (max-width: 768px) {
        .conteudo{
            padding: 130px 0 0 3%;
        }
        .conteudo h1{
            width: 95%;
        }
        .conteudo h4{
            width: 80%;
        }
    }

    @media screen and (max-width: 430px) {
        .conteudo{
            padding: 230px 0 0 3%;
            gap: 50px;
        }
    }
</style>