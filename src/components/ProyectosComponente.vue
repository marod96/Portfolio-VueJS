<template>
    <div class="galeria">
      <li class="proyecto" v-for="proyecto in misProyectos" :key="proyecto.id">
        <img :src="proyecto.src" :alt="proyecto.titulo" class="proyecto-img" />
        <div class="proyecto-info">
          <h3>{{ proyecto.titulo }}</h3>
          <p>{{ proyecto.descripcion }}</p>
          <div class="proyecto-links">
            <a :href="proyecto.projectoLink" class="btn-ver-mas" target="_blank" rel="noopener noreferrer">Ver Proyecto</a>
            <a :href="proyecto.githubLink" class="github-link" target="_blank" rel="noopener noreferrer">Ver Código en GitHub</a>
          </div>
        </div>
      </li>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import proyecto1 from '/src/assets/etb-logo.svg';
  
  const misProyectos = ref([
    {
      id: 1,
      src: proyecto1,
      titulo: "Migración Sistema ETB utilizando Mulesoft",
      descripcion: "Migramos el sistema de facturación de ETB de su plataforma TIBCO a Mulesoft",
      projectoLink: "https://etb.com/",
      githubLink: "https://github.com/marod96"
    }
  ]);
  </script>
  
  <style scoped>
  .galeria {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    padding: 20px;
    background: linear-gradient(-45deg, #021526, #03346E, #6EACDA, #E2E2B6);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
    width: 100%;
  }
  
  .proyecto {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    max-width: 300px;
    padding: 20px;
    text-align: center;
  }
  
  .proyecto-img {
    width: 80%;
    max-height: 150px;
    object-fit: contain;
    margin-bottom: 15px;
  }
  
  .proyecto-info h3 {
    font-size: 1.2rem;
    color: #03346E;
    margin: 10px 0;
  }
  
  .proyecto-info p {
    font-size: 0.9rem;
    color: #333;
    margin-bottom: 15px;
  }
  
  .proyecto-links {
    display: flex;
    flex-direction: column;
    gap: 10px;
    width: 100%;
  }
  
  .btn-ver-mas,
  .github-link {
    display: inline-block;
    padding: 10px;
    color: white;
    background-color: #03346E;
    text-align: center;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease;
  }
  
  .btn-ver-mas:hover,
  .github-link:hover {
    background-color: #005bb5;
  }
  
  @keyframes gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }
  </style>
  