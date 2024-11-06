<script setup>

    import java from '/src/components/icons/java.svg'
    import js from '/src/components/icons/javascript.svg'
    import azure from '/src/components/icons/azure.svg'
    import git from '/src/components/icons/git.svg'
    import github from '/src/components/icons/github.svg'
    import mysql from '/src/components/icons/mysql.svg'
    import postman from '/src/components/icons/postman.svg'
    import python from '/src/components/icons/python.svg'
    import salesforce from '/src/components/icons/salesforce.svg'
    import mulesoft from '/src/assets/mulesoft-icon.svg'


    import { ref } from 'vue';

    const habilidades = ref([
    {// Se crea un objeto con id, nombre y habilidades
        id: 1, nombre: 'Lenguajes de Programación', habilidades: [
            //Se crea un objeto con id, nombre, nivel e icono
            { id: 1, nombre: 'Java', nivel: 'Intermedio', icono: java },
            { id: 2, nombre: 'Python', nivel: 'Básico', icono: python },
            { id: 3, nombre: 'JavaScript', nivel: 'Básico', icono: js }
     
        ]
    },

       {// Se crea un objeto con id, nombre y habilidades
        id: 1, nombre: 'Herramientas y Software', habilidades: [
            //Se crea un objeto con id, nombre, nivel e icono
            { id: 1, nombre: 'Salesforce', nivel: 'Intermedio', icono: salesforce },
            { id: 2, nombre: 'Mulesoft', nivel: 'Intermedio', icono: mulesoft },
            { id: 3, nombre: 'MySQL', nivel: 'Intermedio', icono: mysql },
            { id: 4, nombre: 'Azure Devops', nivel: 'Intermedio', icono: azure },
            { id: 6, nombre: 'Git', nivel: 'Intermedio', icono: git },
            { id: 7, nombre: 'GitHub', nivel: 'Intermedio', icono: github },
            { id: 8, nombre: 'Postman', nivel: 'Intermedio', icono: postman }


        ]
    },


])

</script>

<template>
    <div class="skills-contenedor">
        <!--Se recorre el array habilidades con v-for y se asigna la key habilidad.id-->
        <div v-for="habilidad in habilidades" :key="habilidad.id" class="skills-categoria">
            <!--Se muestra el nombre de la habilidad-->
            <h3>{{ habilidad.nombre }}</h3>
            <ul class="skills">
                <!--Se recorre el array habilidades con v-for y se asigna la key habilidad.id-->
                <li v-for="habilidad in habilidad.habilidades" :key="habilidad.id" class="skill">
                    <!--Se muestra el icono de la habilidad y el nombre de la habilidad con su nivel-->
                    <img :src="habilidad.icono" :alt="habilidad.nombre">
                    <!--Se muestra el icono de la habilidad y el nombre de la habilidad con su nivel-->
                    <span>{{ habilidad.nombre }}: {{ habilidad.nivel }}</span>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.skills-contenedor {
    padding: 2rem;
    /*Fondo cargado desde una imagen estatica en Assets*/
    /* background-image: url('/src/assets/fondo-proyectos.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat; */
    /*Fondo con gradiente*/
    background: linear-gradient(-45deg, #021526, #03346E, #6EACDA, #E2E2B6);
    /*Fondo con color solido*/
    /* background-color: rgb(28, 41, 52); */
}

.skills-categoria {
    margin-bottom: 20px;
}

.skills-categoria h3 {
    display: flex;
    justify-content: left;
    margin-bottom: 10px;
    font-size: 1.5em;
    color: aliceblue;
    font-size: 1.5em;
    font-weight: bold;
}

.skills {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}

.skill {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    background-color: rgba(241, 245, 243, 0.856);
    padding: 0.3em;
    border-radius: 8px;
    box-shadow: 0px 4px 12px rgba(2, 151, 151, 0.963);
    flex: 1 1 200px;
    max-width: 250px;
}

.skill:hover {
    background-color: rgba(2, 151, 151, 0.963);
}

.skill img {
    width: 35px;
    height: 35px;
}

.skill span {
    font-size: 1em;
    color: #333;
}

.skill:hover {
    font-size: 1.3em;
    transition: 2s ease;
}

@media (max-width: 768px) {
    .skills-categoria h3 {
        justify-content: center;
    }

    .skill {
        justify-content: center;
    }
}
</style>