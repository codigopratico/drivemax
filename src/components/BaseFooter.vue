<script setup>
import { ref } from 'vue'

const link_1 = ref('Início')
const link_2 = ref('Serviços')
const link_3 = ref('Depoimentos')
const link_4 = ref('Compra Segura')
const link_5 = ref('Contato')

const copy = ref('2025 DriveMax. Projeto fictício desenvolvido para fins educacionais.')

const local = ref('São Paulo, SP')
const telefone = ref('(00) 98765-4321')
const email = ref('drivemax@gmail.com')
</script>

<template>
    <div class="main">
            <div class="redes">
                <div class="logo">
                    <img src="../assets/img/logo.png" alt="">
                </div>
                <ul class="icones">
                    <li>
                        <i class="bi bi-envelope"></i>
                        <a href="https://github.com/codigopratico" target="_blank">{{ email }}</a>
                    </li>
                    <li>
                        <i class="bi bi-telephone"></i>
                        <a href="https://github.com/codigopratico" target="_blank">{{ telefone }}</a>
                    </li>
                    <li>
                        <i class="bi bi-geo-alt-fill"></i>
                        <a href="https://github.com/codigopratico" target="_blank">{{ local }}</a>
                    </li>
                </ul>
            </div>

            <div class="links">
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
            </div>
            <div class="copy">
                <p>&copy;{{ copy }}</p>
            </div>
    </div>
</template>

<style scoped>
    .main{
        width: 100%;
        background-color: var(--bg-footer);
        padding: 40px 0 20px;
        border-radius: 0px 0 15px 15px;
        box-shadow: -2px -2px 7px 1px rgba(255, 255, 255, 0.3);
    }
    .redes{
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0 35px 0 25px;
    }
    .redes .icones{
        display: flex;
        align-items: center;
        gap: 30px;
    }.icones li{
        display: flex;
        align-items: center;
        gap: 3px;
        font-size: var(--font-body-md);
        cursor: pointer;
        transition: all 200ms;
    }.icones li:hover{
        transform: scale(1.03);
    }
    img{
        height: var(--size-logo);
    }

    .links{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 25px 0 10px 0;
        font-size: var(--font-link-lg);
        border-bottom: 1px solid var(--color-borda);
    }.links a{
        padding: 0 2.5%;
        border-right: 1px solid var(--color-borda);
        transition: all 200ms;
    }.links a:hover{
        transform: scale(1.03);
    }
    #contato{
        border: none;
    }
    .copy{
        display: flex;
        justify-content: center;
        align-items: end;
        height: 35px;
        font-size: 16px;
        font-weight: 400;
    }
    i{
        color: var(--brand-primary);
    }
    i.bi{
        color: var(--text-primary);
    }

    @media screen and (max-width: 850px){
        .redes{
            flex-direction: column;
        }
        .copy{
            height: 35px;
            padding: 0;
        }
    }

    @media screen and (max-width: 785px) {
        .main{
            height: fit-content;
            padding-bottom: 5px;
        }
        .main .redes{
            align-items: start;
        }
        .redes .icones{
            flex-direction: column;
            align-items: start;
        }
        .links{
            flex-direction: column;
            align-items: start;
            padding: 25px 0 25px 12px;
            gap: 25px;
        }.links a{
            border: none;
        }
        .copy{
            padding: 50px 0 0 10px;
        }
        img{
            margin-left: -5px;
            margin-bottom: 10px;
        }
    }
</style>