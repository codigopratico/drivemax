<script setup>
import { ref } from 'vue'

import inspecao from '@/assets/img/secao_3/icone_inspecao.png'
import verificado from '@/assets/img/secao_3/icone_verificado.png'
import negocio from '@/assets/img/secao_3/icone_negocio.png'

const icones = ref([
    {
        id: 1, 
        img: inspecao, 
        alt: 'Inspeção', 
        titulo: 'Inspeção Completa'
    },
    {
        id: 2, 
        img: verificado, 
        alt: 'Verificado',
        titulo: 'Histórico Verificado'
    },
    {
        id: 3, 
        img: negocio, 
        alt: 'Segurança', 
        titulo: 'Negócio Tranparente'
    }
])
</script>

<template>
    <div class="icones">
        <div 
        class="icone"
        v-for="icone in icones"
        :key="icone.id"
        >
            <img 
            :src="icone.img" 
            :alt="icone.alt"
            >
            <h4>{{ icone.titulo }}</h4>
        </div>
    </div>
</template>

<style scoped>
    .icones{
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 45px;
        padding: 15px 10px;
        flex-wrap: wrap;
        padding: 0 5px;
    }
    .icone{
        display: flex;
        flex-direction: column;
        align-items: center;
        flex: 1 1 200px;
        max-width: 300px;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        padding: 10px;
        border-radius: 15px;
        background-color: var(--bg-card);
        box-shadow: 5px 5px 10px 1px rgba(0, 0, 0, 0.4);
        transition: all 300ms;
    }
    .icone:hover{
        transform: scale(1.02);
        box-shadow: 5px 5px 10px 1px rgba(255, 255, 255, 0.15);
    }
    h4{
        font-size: var(--font-body-md);
        padding-top: 10px;
        color: var(--bg-page);
    }
    img{
        height: clamp(120px, 4vh, 160px);
        width: fit-content;
    }

    @media screen and (max-width: 600px) {
        .icones{
            padding: 25px 0;
            gap: 55px;
        }
    }

</style>