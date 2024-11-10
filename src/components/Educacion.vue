<script setup>
import { ref } from 'vue';

const arreglo = ref([
    { id: 1, fecha: "2024", titulo: "Estudiante de la Tecnicatura 2024 - UTN SAN RAFAEL", descripcion: "Estudios en programación con enfoque en Java, Python y JavaScript." },
    { id: 2, fecha: "2023", titulo: "Curso de React.js", descripcion: "Finalización de un curso avanzado en desarrollo de aplicaciones front-end con React." },
    { id: 3, fecha: "2022", titulo: "Curso de Auxiliar de Farmacia - Instituto Newton", descripcion: "Obtención de conocimientos básicos en farmacia y farmacología." },
    { id: 4, fecha: "2021", titulo: "Curso de Desarrollo Web - Coderhouse", descripcion: "Aprendizaje de HTML, CSS y JavaScript para desarrollo web básico." },
    { id: 5, fecha: "2020", titulo: "Secundario Completo", descripcion: "Finalización de estudios de nivel medio." }
]);
</script>

<template>
  <h1>Linea de Tiempo</h1>
  <div class="timeline">
    <div v-for="(item, index) in arreglo" :key="item.id" class="timeline-item" :class="{ 'left': index % 2 === 0, 'right': index % 2 !== 0 }">
      <div class="content">
        <div class="fecha">{{ item.fecha }}</div>
        <div class="titulo">{{ item.titulo }}</div>
        <div class="descripcion">{{ item.descripcion }}</div>
        <div class="enlace">
          <a href="#">Ver más detalles</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
h1{
    color: white;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

.timeline {
    position: relative;
    margin: 2rem 0;
    padding: 1rem;
    border-left: 3px solid #a54646;
}

.timeline-item {
    position: relative;
    width: 45%;
    margin: 1rem 0;
    padding: 1rem;
    background-color: #f3c8c8;
    border: 1px solid #c55e5e;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.timeline-item.left {
    left: 0;
}

.timeline-item.right {
    left: 55%;
}

.timeline-item::before {
    content: '';
    position: absolute;
    top: 1rem;
    left: -1.5rem;
    width: 10px;
    height: 10px;
    background-color: #974646;
    border-radius: 50%;
    border: 3px solid #d15353;
}

.timeline-item.left::after,
.timeline-item.right::after {
    content: '';
    position: absolute;
    top: 0;
    left: -3px;
    height: 100%;
    width: 3px;
    background-color: #a52727;
}

.timeline-item.right::after {
    left: auto;
    right: -3px;
}

.content .fecha {
    font-weight: bold;
    color: #333;
    margin-bottom: 0.5rem;
}

.content .titulo {
    font-size: 1.1rem;
    color: #000000;
    margin-bottom: 0.5rem;
}

.content .descripcion {
    color: #555;
    margin-bottom: 0.5rem;
}

.enlace {
    text-align: right;
}

.enlace a {
    color: #0056b3;
    text-decoration: none;
}

.enlace a:hover {
    text-decoration: underline;
}
</style>
