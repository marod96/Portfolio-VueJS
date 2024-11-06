<script setup>

import DatosPersonales from './components/DatosPersonales.vue';
import NavBar from './components/NavBar.vue';
import Educacion from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosComponente from './components/ProyectosComponente.vue';
import HabilidadesComponente from './components/HabilidadesComponente.vue';
</script>

<template>
  <header>
  <!--Barra de Navegación-->
    <NavBar></NavBar>

    <!--Componente de Datos Personales-->
    <DatosPersonales></DatosPersonales>


  </header>
  <main>

    <section id="educacion">
      <h2>Educacion - Cursos</h2>
      <!--Componente de Datos Personales-->
      <Educacion></Educacion>
    </section>

    <section id="experiencia">
      <h2>Experiencia</h2>
      <!--Componente de Experiencia-->
      <ExperienciaComponente></ExperienciaComponente>
    </section>

    <section id="proyectos">
      <h2>Proyectos</h2>
       <!--Componente de Proyectos-->
      <ProyectosComponente></ProyectosComponente>
    </section>


    <section id="habilidades"><h2>Habilidades</h2>
    <!--Componente de Habilidades-->
    <HabilidadesComponente></HabilidadesComponente>
    </section>
    <section id="intereses"><h2>Intereses</h2></section>
  </main>

</template>



<style scoped>

</style>