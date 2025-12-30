<script setup>

const props = defineProps({
    servicos: {
        type: Array,
        required: true
    }
})
</script>

<template>
    <div class="cards">
        <div 
        class="card"
        v-for="servico in props.servicos" 
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
        padding: 10px 15px;
        gap: 10px;
        align-items: center;
        height: 350px;
        flex: 1 1 260px;
        max-width: 300px;
        text-align: center;
        box-shadow: 10px 4px 20px rgba(0, 0, 0, 0.2);
        background-color: var(--bg-card);
        border-radius: 15px;
        transition: ease-in-out 300ms;
    }.card:hover{
        transform: scale(1.01);
        box-shadow: 10px 4px 20px rgba(255, 255, 255, 0.2);
    }
    .texto{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 25px;
        width: 100%;
    }
    h2, p{
        color: var(--text-dark);
    }
    h2{
        font-size: var(--font-title-sm);
        min-width: 280px;
    }
    p{
        font-size: var(--font-body-md);
    }
    img{
        width: fit-content;
        height: 140px;
    }

    @media screen and (max-width: 768px) {
        h2{
            min-width: none;
        }
    }
</style>