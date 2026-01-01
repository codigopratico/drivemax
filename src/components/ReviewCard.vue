<script setup>
import { ref } from 'vue'

import homem from '@/assets/img/secao_4/depoimento_masculino.png'
import mulher from '@/assets/img/secao_4/depoimento_feminino.png'

const avaliacoes = ref([
    {
        id: 1, 
        img: homem, 
        alt: 'Homem', 
        nome: 'Carlos S.', 
        comentario: '"Achei o carro perfeito e negociei sem dor de cabeça. Fantástico!"'
    },
    {
        id: 2,
        img: mulher,
        alt: 'Mulher',
        nome: 'Mariana L.',
        comentario: '"A DriveMax me deu muita segurança na compra. Recomendo a todos!"'
    }
])
</script>

<template>
    <div class="avaliacoes">
        <div 
        class="avaliacao"
        v-for="avaliacao in avaliacoes"
        :key="avaliacao.id"
        > 
            <div class="perfil">
                <img :src="avaliacao.img" :alt="avaliacao">
                <div class="informacoes">
                    <h2>{{ avaliacao.nome }}</h2>
                    <div class="icones">
                        <i class="bi bi-star-fill"></i>
                        <i class="bi bi-star-fill"></i>
                        <i class="bi bi-star-fill"></i>
                        <i class="bi bi-star-fill"></i>
                        <i class="bi bi-star-fill"></i>
                    </div>
                </div>
            </div>
            <div class="comentario">
                <p>{{ avaliacao.comentario }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .avaliacoes{
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 35px;
        flex-wrap: wrap;
        padding: 0 10px;
    }
    .avaliacao{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 25px;
        padding: 25px 10px;
        min-width: 200px;
        max-width: 380px;
        border-radius: 15px;
        box-shadow: 5px 5px 20px rgba(0, 0, 0, 0.5);
        min-height: 420px;
        max-height: 700px;
        background-color: var(--bg-card);
        transition: all 300ms;
    }
    .avaliacao:hover{
        transform: scale(1.02);
        box-shadow: 5px 5px 10px 1px rgba(255, 255, 255, 0.15);
    }
    .perfil{
        display: flex;
        align-items: center;
        gap: 10px;
    }
    .informacoes{
        display: flex;
        align-items: center;
        flex-direction: column;
        text-align: center;
    }
    img{
        height: 160px;
        width: fit-content;
        border-radius: 50%;
        box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.35);
    }
    .icones{
        display: flex;
        gap: 3px;
    }
    i{
        color: var(--star);
        font-size: 20px;
        box-shadow: 5px 5px 25px rgba(255, 255, 255, 0.15);
    }
    h2, p{
        color: var(--bg-page);
    }
    .comentario{
        width: clamp(80%, 5vw, 85%);
    }
    h2{
        font-size: var(--font-subtitle-lg);
        text-shadow: 5px 5px 25px rgba(255, 255, 255, 1);
    }
    p{
        font-size: var(--font-comment);
    }

    @media screen and (max-width: 768px) {
        .avaliacao{
            min-height: 260px;
            max-width: 335px;
        }
    }
</style>