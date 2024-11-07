<template>
    <!-- Barra de Navegación -->
    <nav class="navbar">
      <div class="navbar-menu">
        <ul>
          <a v-for="nav in navegacion" :key="nav.nombre" :href="nav.enlace" class="nav-item">{{ nav.nombre }}</a>
        </ul>
      </div>
    </nav>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  const navegacion = ref([
    { id: 1, nombre: 'Educación', enlace: '#educacion' },
    { id: 2, nombre: 'Experiencia', enlace: '#experiencia' },
    { id: 3, nombre: 'Proyectos', enlace: '#proyectos' },
    { id: 4, nombre: 'Habilidades', enlace: '#habilidades' },
    { id: 5, nombre: 'Intereses', enlace: '#intereses' }
  ]);
  </script>
  
  <style scoped>
  .navbar {
    position: fixed;
    top: 0;
    width: 75%; /* Asegura que el navbar ocupe el ancho completo */
    background-color: #003366;
    color: #fff;
    padding: 0.5rem 1rem;
    display: flex;
    justify-content: center;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    z-index: 1000;
  }
  
  .navbar-menu {
    display: flex;
    width: 100%; /* Asegura que el menú ocupe el ancho completo */
    justify-content: center; /* Centra los elementos en el menú */
  }
  
  ul {
    display: flex;
    gap: 20px;
    list-style: none;
    padding: 0;
    margin: 0; /* Elimina el margen para que ocupe el ancho completo */
  }
  
  .nav-item {
    color: #ffffff;
    padding: 10px 20px;
    background-color: #005599;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease;
  }
  
  .nav-item:hover {
    background-color: #0077cc;
  }
  
  @media (max-width: 768px) {
    .navbar {
      justify-content: center;
    }
  }
  </style>
  