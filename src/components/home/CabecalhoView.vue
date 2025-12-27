<script setup>
import { ref } from 'vue'


const link_1 = ref('Início')
const link_2 = ref('Serviços')
const link_3 = ref('Depoimentos')
const link_4 = ref('Como Funciona')
const link_5 = ref('Contato')
const btn = ref('AGENDAR CONSULTORIA')

const responsivo = ref(false)

const toggle = () => {
    responsivo.value = !responsivo.value
}
</script>

<template>
    <header class="cabecalho" :class="{active: responsivo}">
        <div class="logo">
            <img src="../../assets/img/logo.png" alt="">
            <div class="icone_menu">
            <i class="bi bi-list" 
            @click="toggle" 
            v-show="!responsivo"></i>

            <i class="bi bi-x-lg"
            @click="toggle"
            v-show="responsivo"></i>
        </div>
        </div>
        <div :class="{navigation: !responsivo, menu: responsivo}">
            <nav class="links">
                <a href="#">{{ link_1 }}</a>
                <a href="#">{{ link_2 }}</a>
                <a href="#">{{ link_3 }}</a>
                <a href="#">{{ link_4 }}</a>
                <a href="#">{{ link_5 }}</a>
            </nav>
            <div class="butao">
                <button>{{ btn }}</button>
            </div>
        </div>
    </header>
</template>

<style scoped>
    .cabecalho{
        background: transparent;
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 90px;
        padding: 0 25px;
        top: 0;
        left: 0;
        position: absolute;
        box-sizing: border-box;
        inset: 0;
        z-index: 2;
    }
    .navigation{
        display: flex;
        align-items: center;
        gap: 12px;
    }
    .icone_menu{
        display: none;
    }.logo{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .logo img{
        height: var(--img-logo);
        box-shadow: 0 4px 20px rgba(255, 255, 255, 0.02);
    }
    .links{
        display: flex;
        gap: 12px;
    }.links a{
        border-right: 2px solid var(color-borda);
        padding: 5px 10px 5px 10px;
        font-size: var(--text-link);
        text-shadow: 10px 10px 25px #1f1f1f;
    }.links a:focus{
        border-bottom: 3px solid var(--color-laranja);
        box-shadow: 0 4px 20px rgba(255, 255, 255, 0.2);
        border-radius: 7px;
    }
    button{
        margin-left: 6px;        
    }
    i{
        font-size: 33.5px;
        cursor: pointer;
        padding: 5px;
    }

    /* Menu resposivo */
    @media screen and (max-width: 1100px) {
        .cabecalho{
            flex-direction: column;
            padding: 10px 22px;
            height: fit-content;
        }.active{
            background-color: var(--color-preto);
        }
        .icone_menu{
            display: block;
        }
        .logo{
            padding: 7px 10px;
            width: 100%;
        }
        .navigation{
            display: none;
        }
        .menu{
            display: flex;
            flex-direction: column;
            padding: 10px 0;
            align-items: center;
            width: 100%;
            max-width: 100%;
            box-sizing: border-box;
        }
        .links{
            flex-direction: column;
            align-items: left;
            padding-bottom: 10px;
            gap: 10px;
            padding: 0 5px 15px 5px;
            width: 100%;
        }
        .links a{
            font-size: var(--text-link-responsivo);
            border-bottom: 1px solid var(--color-branco);
            padding: 5px 0px 10px 5px;
            border-right: none;
        }.links a:focus{
            padding: 10px 0px 10px 5px;
        }
        .logo img{
            box-shadow: none;
        }
        button{
            font-size: var(--text-butao-responsivo);
            margin-top: 10px;
        }
    }
    @media screen and (max-width: 475px) {
        .cabecalho{
            padding: 10px 10px 0 10px;
        }
    }
</style>