<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/Educacion.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosComponentes from './components/ProyectosComponentes.vue';
import HabilidadesComponentes from './components/HabilidadesComponentes.vue';
import InteresesComponente from './components/InteresesComponente.vue';
</script>

<template>
  <header>
    <!--Barra de navegacion-->
    <NavBar />
    <!--Componente Datos Personales-->
    <DatosPersonales/> 
  </header>
  <main>
    <section id ="educacion"><h2>Educacion - Cursos</h2></section>
    <!--Educacion-->
    <Educacion/>
    <section id ="experiencia"><h2>Experiencia</h2></section>
    <ExperienciaComponente/>
    <section id ="proyectos"><h2>Proyectos</h2></section>
    <!--Componente Proyecto -->
    <ProyectosComponentes/>
    <section id ="habilidades"><h2>Habilidades</h2></section>
    <!--Componente Habilidades-->
    <HabilidadesComponentes/>
    <section id ="intereses"><h2>Intereses</h2></section>
    <!--Componente Intereses-->
    <InteresesComponente/>
  </main>
</template>

<style scoped>
h2{
  color: white;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

</style>
