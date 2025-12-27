<script setup>
import { ref } from 'vue'
import RodapeView from './chamada/RodapeView.vue';

const titulo = ref('PRONTO PARA COMPRAR SEU CARRO IDEAL?')
const subtitulo = ref('Deixe a DriveMax guiar você até a melhor escolha!')
const btn1 = ref('AGENDAR CONSULTORIA')
const btn2 = ref('FALAR COM UM ESPECIALISTA')

</script>

<template>
    <div class="principal">
        <div class="acao">
            <div class="texto">
                <h1>{{ titulo }}</h1>
                <h4>{{ subtitulo }}</h4>
            </div>
            <div class="butoes">
                <button>{{ btn1 }}</button>
                <button id="btn2">{{ btn2 }}</button>
            </div>
        </div>
        <RodapeView />
    </div>
</template>

<style scoped>
    .principal{
        width: 100%;
        background-color: var(--color-fundo-branco);
        border-radius: 15px;
        padding: 40px 0 0 0;
    }
    .acao{
        display: flex;
        flex-direction: column;
        gap: 40px;
        align-items: center;
        padding: 35px 0;
    }
    .texto{
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: center;
    }
    h1, h4{
        color: var(--color-preto-texto);
    }
    .texto h1{
        font-size: var(--text-titulo-secundario);
    }
    .texto h4{
        font-size: var(--text-subtitulo-secundario);
        font-weight: 400;
    }
    .butoes{
        display: flex;
        gap: 5px;
    }
    #btn2{
        background-color: var(--color-texto-secundario);
        border: 1px solid var(--color-preto);
    }
    button{
        font-size: var(--text-butao-principal);
    }

    @media screen and (max-width: 550px){
        .acao{
            padding: 15px 0 15px 5px;
        }
        .texto{
            align-items: start;
        }
        .butoes{
            padding: 10px;
            width: 100%;
            flex-direction: column;
            align-items: start;
        }
    }
</style>