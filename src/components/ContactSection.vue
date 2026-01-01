<script setup>
import { ref} from 'vue'
import BaseFooter from './BaseFooter.vue';

const titulo = ref('PRONTO PARA COMPRAR SEU CARRO IDEAL?')
const subtitulo = ref('Deixe a DriveMax guiar você até a melhor escolha!')
const btn1 = ref('NEGOCIAR SEGURO')
const btn2 = ref('FALAR COM CONSULTOR')

</script>

<template>
    <div class="principal">
        <div class="acao">
            <div class="texto">
                <h1>{{ titulo }}</h1>
                <h4>{{ subtitulo }}</h4>
            </div>
            <div class="butoes">
                <button><a href="https://github.com/codigopratico" target="_blank">{{ btn1 }}</a></button>
                <button id="btn2"><a href="https://github.com/codigopratico" target="_blank">{{ btn2 }}</a></button>
            </div>
        </div>
        <BaseFooter />
    </div>
</template>

<style scoped>
    .principal{
        width: 100%;
        background-color: var(--bg-section-dark);
        border-radius: 15px;
        padding: 40px 0 0 0;
    }
    .acao{
        display: flex;
        flex-direction: column;
        gap: 40px;
        align-items: center;
        padding: 35px 0;
        background-color: var(--bg-section-light);
    }
    .texto{
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: center;
        text-align: center;
    }

    .texto h1{
        font-size: var(--font-heading-lg);
        color: var(--text-dark);
    }
    .texto h4{
        color: var(--text-dark);
        font-size: var(--font-subtitle-md);
        font-weight: 400;
    }
    .butoes{
        display: flex;
        gap: 15px;
    }
    #btn2{
        background-color: var(--text-muted);
        border: 1px solid var(--border-default);
    }
    button{
        font-size: var(--font-button-lg);
        border: 1px solid var(--text-dark);
    }
    button a{
        padding: 10px;
    }

    @media screen and (max-width: 550px){
        .acao{
            padding: 15px 0 15px 5px;
        }
        .texto{
            text-align: start;
            align-items: start;
            padding: 10px;
        }
        .butoes{
            padding: 10px;
            width: 100%;
            flex-direction: column;
            align-items: start;
        }
    }
</style>