<script setup>
import { ref } from 'vue';
import FondoIntereses from './FondoIntereses.vue';
const intereses = ref([
    'Aprender nuevos lenguajes y tecnologías,esto me gusta ya que mantenerme al tanto con las tecnologias nuevas, me hace sentir mas profesional en mis ambitos laborales.',
    'Deportes, me gusta mucho ir al gimnasio y entrenar pesas.Jugar Futbol y compartir de cualquier actividad en conjunto con amigos.',
    'VideoJuegos, soy muy apasionado por los videojuegos, tambien muy competitivo. Me gusta disfrutar de mi tiempo libre con esta manera de entretenimiento.',
    'Cocinar, me gusta cocinar como hobby, probar cosas nuevas ,poder compartirlo con amigos o familia..'
]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoIntereses />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
    <!-- <div class="intereses-contenedor">
        <ul class="contenedor-lista">
            <li class="item">
                Desarrollo de Software de Código Abierto: Contribuyo a proyectos en GitHub, colaborando con otros
                desarrolladores para mejorar herramientas y librerías populares.
            </li>
            <li class="item">
                Deportes al Aire Libre: Disfruto del senderismo y el ciclismo de montaña, actividades que practico
                regularmente para mantener un equilibrio entre el trabajo y la vida personal.
            </li>
            <li class="item">
                Tecnología de Innovación: Me apasiona explorar nuevas tendencias tecnológicas como la inteligencia
                artificial y el desarrollo de aplicaciones móviles.
            </li>
            <li class="item">
                Fotografía: Practico la fotografía como un hobby, lo que me ayuda a mantener una perspectiva creativa
                tanto en mi vida profesional como personal.
            </li>
        </ul>
    </div> -->
</template>

<style scoped>
.intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}
</style>