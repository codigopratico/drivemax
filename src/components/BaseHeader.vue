<script setup>
import { ref } from 'vue'


const link_1 = ref('Início')
const link_2 = ref('Serviços')
const link_3 = ref('Depoimentos')
const link_4 = ref('Compra Segura')
const link_5 = ref('Contato')
const btn = ref('NEGOCIAR SEGURO')

const responsivo = ref(false)

const toggle = () => {
    responsivo.value = !responsivo.value
}
</script>

<template>
    <header class="cabecalho" :class="{active: responsivo}">
        <div class="logo">
            <img src="../assets/img/logo.png" alt="">
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
                <a href="#home">
                    <i class="bi bi-house-fill"></i>
                    {{ link_1 }}
                </a>
                <a href="#services">
                    <i class="bi bi-briefcase-fill"></i>
                    {{ link_2 }}
                </a>
                <a href="#review">
                    <i class="bi bi-chat-dots-fill"></i>
                    {{ link_3 }}
                </a>
                <a href="#security">
                    <i class="bi bi-shield-fill-check"></i>
                    {{ link_4 }}
                </a>
                <a href="#contact">
                    <i class="bi bi-telephone-fill"></i>
                    {{ link_5 }}
                </a>
            </nav>
            <div class="butao">
                <button><a href="https://github.com/codigopratico" target="_blank">{{ btn }}</a></button>
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
    .menu{
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
        height: var(--size-logo);
        box-shadow: 0 4px 20px rgba(255, 255, 255, 0.02);
    }
    .links{
        display: flex;
        gap: 12px;
    }.links a{
        border-right: 2px solid var(color-borda);
        padding: 5px 10px 5px 10px;
        font-size: var(--font-link-md);
        text-shadow: 1px 1px 25px #1f1f1f;
        display: flex;
        align-items: center;
        gap: 3px;
        transition: all 200ms;
    }.links a:focus{
        border-bottom: 3px solid var(--brand-primary);
        box-shadow: 0 4px 20px rgba(255, 255, 255, 0.2);
        border-radius: 7px;
    }.links a:hover{
        transform: scale(1.02);
        text-shadow: 3px 3px 12px #1f1f1f;
    }
    button{
        margin-left: 6px;        
    }
    button a{
        padding: 10px;
    }
    i{
        font-size: 33.5px;
        cursor: pointer;
        padding: 5px;
    }
    i.bi{
        font-size: 26px;
        color: var(--text-primary);
    }

    /* Menu resposivo */
    @media screen and (max-width: 1300px) {
        .cabecalho{
            flex-direction: column;
            padding: 10px 22px;
            height: fit-content;
        }.active{
            background-color: var(--bg-page);
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
            gap: 0;
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
            font-size: var(--font-link-lg);
            border-bottom: 1px solid var(--border-default);
            padding: 5px 0px 10px 5px;
            border-right: none;
        }.links a:focus{
            padding: 10px 0px 10px 5px;
        }
        .logo img{
            box-shadow: none;
        }
        button{
            font-size: var(--font-button-lg);
            margin-top: 10px;
        }
    }
    @media screen and (max-width: 475px) {
        .cabecalho{
            padding: 10px 10px 0 10px;
        }
    }
</style>