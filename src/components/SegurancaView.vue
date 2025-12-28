<script setup>
import { ref } from 'vue'

import IconesView from './seguranca/IconesView.vue';

const titulo = ref('COMPRE SEU CARRO COM SEGURANÇA')
const texto = ref('Tenha a tranquilidade de fazer um bom negócio sem surpresas.')
const btn1 = ref('AGENDAR CONSULTORIA')
const btn2 = ref('FALAR COM UM ESPECIALISTA')
</script>

<template>
    <div class="main">
        <div class="titulo">
            <h1>{{ titulo }}</h1>
        </div>
        <div class="texto">
            <h3>{{ texto }}</h3>
        </div>
        <IconesView />
        <div class="imagens">
            <div class="img">
            </div>
            <div class="img2">
                <button>{{ btn1 }}</button>
                <button id="secundario">{{ btn2 }}</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .main{
        width: 100%;
        background-color: var(--color-fundo-branco);
        border-radius: 15px;
        display: flex;
        flex-direction: column;
        gap: 35px;
        align-items: center;
        justify-content: center;
        position: relative;
    }
    .imagens{
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 7px;
        background-color: var(--color-laranja);
        border-radius: 15px;
    }
    .img{
        max-height: 100vh;
        min-height: 50vw;
        width: 100%;
        background-image: url('../assets/img/secao_3/Consultor_casal.png');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center top;
        border-radius: 15px 15px 0 0;
    }.img2{
        max-height: 100vh;
        min-height: 50vw;
        width: 100%;
        background-image: url('../assets/img/secao_3/Carro_fundo.png');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: bottom right;
        display: flex;
        align-items: end;
        justify-content: center;
        gap: 10px;
        padding-bottom: clamp(20px, 3vw, 45px);
        border-radius: 0 0 15px 15px;
    }
    h3{
        color: var(--color-preto);
        font-size: var(--text-servicos-titulo);
    }
    button{
        font-size: var(--text-butao-responsivo);
        border: 1px solid var(--color-branco);
    }
    #secundario{
        background-color: var(--color-texto-secundario);
    }

    @media screen and (max-width: 600px){
        .img2{
            flex-direction: column;
            align-items: center;
            justify-content: end;
        }
    }
</style>