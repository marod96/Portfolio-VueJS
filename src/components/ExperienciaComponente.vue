<script setup>
import icono1 from '/src/assets/mulesoft-icon.svg';


import { ref } from 'vue';
const titulo = 'Desarrollador Mulesoft - GLOBANT ';
const fecha = 'Abril 2022 - Septiembre 2023';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Desarrollo de APIs en Design Center desde cero.'},
    { id: 2, src: icono1, parrafo: 'Maquetación y construcción de APIs con RAML.'},
    { id: 3, src: icono1, parrafo: 'Desarrollo de APIs en Design Center desde cero.'},
    { id: 4, src: icono1, parrafo: 'Testing de funcionalidades utilizando la herramienta Postman'},
    { id: 5, src: icono1, parrafo: 'Documentación de Funcionalidades en Azure Devops.'},

]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>

        <ul class="listado">

            <li class="item" v-for="experiencia in experiencias" :key="experiencia.id">
                <img class="imagen-svg" :src="experiencia.src" width="45rem" :alt="experiencia.parrafo">
                <p>{{ experiencia.parrafo }}</p>
            </li>

        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: rgb(26, 123, 243);
}

.fecha {
    font-size: 1rem;
    color: burlywood;
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

</style>