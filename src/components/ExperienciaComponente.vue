<script setup>
import{ref} from 'vue';
const titulo = "Desarrollador Web";
const fecha = "Desde Noviembre 2021 / Noviembre 2024";
const experiencias = ref([
    { id: 1, src:"/src/assets/python.svg", parrafo: 'Python: Data Scientist en una Startup de Fintech.' },
    { id: 2, src: "/src/assets/js.svg", parrafo: 'JavaScript: Desarrollador Frontend en una Agencia de Publicidad Digital.' },
    { id: 3, src: "/src/assets/java.svg", parrafo: 'Java: Desarrollador Backend en un Banco.' },
    { id: 4, src: "/src/assets/git.svg", parrafo: 'Desarrollador Frontend en una Startup de Fintech con Git y Vue.' },
    { id: 5, src: "/src/assets/vue.svg", parrafo: 'Desarrollador Full-Stack en una Agencia de Diseño Web con Git y Vue.' },
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{titulo}}</h3>
        <p class="fecha">{{fecha}}</p>
        <ul class="listado">
            <li class="item" v-for="experiencia in experiencias" :key="experiencia.id">
                <img class="imagen-svg" :src="experiencia.src" width="45rem" :alt="experiencia.parrafo">
                <p>{{ experiencia.parrafo }}</p>
            </li>
        
            <!--li class="item"><img class="imagen-svg" src="/src/assets/python.svg" width="45rem" alt="">
                <p>Python: Data Scientist en una Startup de Fintech</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/js.svg" width="45rem" alt="">
                <p>JavaScript: Desarrollador Frontend en una Agencia de Publicidad Digital</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/java.svg" width="45rem" alt="">
                <p>Java: Desarrollador Backend en un Banco</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/git.svg" width="45rem" alt="">
                <p>Desarrollador Frontend en una Startup de Fintech con Git y Vue</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/vue.svg" width="45rem" alt="">
                <p>Desarrollador Full-Stack en una Agencia de Diseño Web con Git y Vue</p>
            </li>-->
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: #f7aeac;
    border-radius: 15px;
    color: black;
}

.titulo {
    font-size: 1.5rem;
    color: rgb(0, 0, 0);
}

.fecha {
    font-size: 1rem;
    color: rgb(255, 255, 255);
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
.experiencias.parrafo{
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(247, 174, 172);
    border-radius: 15px;
}
</style>