<script setup>
import proyecto1 from '/src/assets/proyecto1(1).jpg';
import proyecto2 from '/src/assets/proyecto2.jpg';
import proyecto3 from '/src/assets/proyecto3.jpg';
import proyecto4 from '/src/assets/proyecto4.jpg';
import { ref } from 'vue';
var misProyectos = ref([]);

misProyectos.value = ([
    {
        id: 1,
        src: proyecto1,
        titulo: "Aplicación web de comercio electrónico con Python (Django)(2023)",
        descripcion: "Creé una aplicación web con caracteristicas como el catalogo de productos, carrito de compras, procedimiento de pago, control de stock y panel de administracion.",
        projectoLink: "https://www.google.com.ar",
        githubLink: "https://github.com/usuario/proyecto"
    },
    {
        id: 2,
        src: proyecto2,
        titulo: "Juego web 2D con Phaser (JavaScript) (2022)",
        descripcion: "Diseñé y desarrollé un videojuego web con Phaser.",
        projectoLink: "https://www.google.com.ar",
        githubLink: "https://github.com/usuario/proyecto"   
    },
    {
        id: 3,
        src: proyecto3,
        titulo: "Visualizador de datos con Python (Dash) y React(2024)",
        descripcion: "Desarrolle un visualizador de datos, creando asi graficos interactivos y personalizados, exportando datos y visualizando graficos.",
        projectoLink: "https://www.google.com.ar",
        githubLink: "https://github.com/usuario/proyecto"  
    },
    {
        id: 4,
        src: proyecto4,
        titulo: "Red Social con Node.js y React",
        descripcion: "Desarrolle una plataforma para conectar con amigos y familiares, compartir contenido y crear comunidades.",
        projectoLink: "https://www.google.com.ar",
        githubLink: "https://github.com/usuario/proyecto"  
    },
])
 </script>


<template>
    <div class="galeria">
        <li class="proyecto" v-for="proyecto in misProyectos" :key="proyecto.id">
            <img :src="proyecto.src" :alt="proyecto.titlulo">
            <div class="proyecto-info">
            <h3>{{ proyecto.titulo }}</h3>
            <p>{{ proyecto.descripcion }}</p>
                <div class="proyecto-links">
            <a :href="proyecto.projectoLink" class="btn-ver-mas" target="_blank" rel="noopener noreferrer">Ver
                        Proyecto</a>
                    <a :href="proyecto.githubLink" class="github-link" target="_blank" rel="noopener noreferrer">Ver
                        Código en GitHub</a>
                </div>
            </div>
        </li>
    </div>
</template>




<style scoped>
 .galeria{
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    background-image: url('/src/assets/fondoproyecto.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
 }
.proyecto {
    display: flex;
    flex-direction: column;
    border: 2px solid #fd0404;
    border-radius: 8px;
    overflow: hidden;
    background-color: #f5bebe;
    max-width: 222px;
    flex: 1 1 300px;
}
.proyecto img {

    width: 100%;
    height: auto;
    display: block;
}

.proyecto-info {
    padding: 15px;
    text-align: center;
}

.proyecto-info h3 {
    margin: 10px 0;
    font-size: 1.3em;
    color: #333;
}

.proyecto-info p {
    margin: 10px 0;
    font-size: 1em;
    color: #666;
}

.proyecto-links {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-top: 30px;

}

.proyecto-links .btn-ver-mas {
    background-color: #d41212;
    color: #fff;
    padding: 10px 15px;
    border-radius: 5px;
    text-decoration: none;
    transition: background-color 0.3s;
    margin-top: 1rem;
}

.proyecto-links .btn-ver-mas:hover {
    background-color: #c45567;
}

.proyecto-links .github-link {
    color: #000000;
    text-decoration: none;
    font-size: 0.9em;
}


.proyecto-links .github-link:hover {
    text-decoration: underline;
}

</style>