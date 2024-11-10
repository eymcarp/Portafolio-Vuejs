<script setup>
const title = 'Mauro Ulloa';
const descripcion = 'Estudiante Universitario, Tecnicatura en Programacion - UTN';
const residencia = 'Godoy Cruz, Mendoza, Argentina';
const presentacion = 'Hola, bienvenido a mi portafolio de proyectos, que habla un poco sobre mi y otras por chatgpt :).';
const redesSociales = [
  { id: 1, name: 'linkedin', src: '/src/assets/linkedin_icon.svg', url: 'https://www.linkedin.com/in/mauro-ulloa-3078b1175/' },
  { id: 2, name: 'Instagram', src: '/src/assets/instagram_icon.svg', url: 'https://www.instagram.com/mauroulloa14/' },
  { id: 3, name: 'github', src: '/src/assets/github_icon.svg', url: '' },
  { id: 4, name: 'curriculum', src:'/src/assets/cv_resume_icon.svg', url: '' },
];
const telefono = '+54 9 2040-255050';
</script>

<template>
    <section class="datos-personales">  
        <div class="card">
            <h1>{{ title }}</h1>
            <h2>{{descripcion}}</h2>
            <p> {{ presentacion }}</p>
            <ul class="container-lista">
            <li v-for="red in redesSociales" :key="red.id">
                <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" alt="red.name"></a>
                </li>
            </ul>
            <h3> Mi telefono personal: {{ telefono }}</h3>
            <h4>{{residencia}}</h4>
        </div>
    </section>
</template>

<style scoped>
.content .title{
  font-size: 1.1rem;
    color: #000000;
    margin-bottom: 0.5rem;
}
.content .descripcion{
  font-size: 1.1rem;
    color: #000000;
    margin-bottom: 0.5rem;
}
.content.descripcion{
  font-size: 1.1rem;
    color: #000000;
    margin-bottom: 0.5rem;
}
h1 {
  font-size: 2.5rem;
  color: white;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

p {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 1rem;
  color: white;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.card {
  background-color: #c77070;
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  text-align: center;
  color: black;
  
}

.container-lista {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;
}

.icon-redsocial {
  align-items: center;
  background-color: aliceblue;
  border-radius: 50%;
  padding: 2px;
  margin: 5px;
  box-shadow: 0 0 5px rgba(14, 78, 253, 0.934);
}

.icon-redsocial:hover {
  background-color: rgb(28, 41, 52);
  box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3 {
  font-size: 1.2rem;
  font-weight: 600;
  color: white;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
h4{
  color: white;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
h2{
  color: white;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
</style>