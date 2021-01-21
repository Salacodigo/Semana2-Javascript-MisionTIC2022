<template>
  <div id="app">
  <div class="container-fluid p-5" id="news">
          <api></api>
    </div>

      <div class="container-fluid" id="team">
        <div class="row justify-content-center mb-5">
          <div class="col mt-5" v-for="(item,index) of team" :key=index>
            <TeamCard v-bind:member="item"> </TeamCard>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import Api from "./components/Api.vue";

import TeamCard from './components/TeamCard.vue'

export default {

  name: 'App',
  components:{
    Api,
    TeamCard
  },
  data()
  {
    return{
      team: [
        {
          codigo: 1,
          nombre: "Gustavo Adolfo Gomez Calderón",
          descripcion: 
          "Ingeniero civil y docente del magisterio. Me gusta aprender y mejorar cada día más.",
          rol: "Desarrollador Backend",
          imagen: "./gustav.jpeg"
        },
        {
          codigo: 2,
          nombre: "Mariver Milena Garcia Santana",
          descripcion:"Ingeniera de Sistemas especialista en redes, docente de la IED República de Francia en San Francisco.",
          rol: "Desarrollador Backend",
          imagen: "./milena.jpeg"
        },
        {
          codigo: 3,
          nombre: "Harold Isaias Sanchez Cabezas",
          descripcion:"Ingeniero Electrónico, tengo 26 años, me dedico a ampliar mis conocimientos para una buena oferta laboral.",
          rol: "Desarrollador Backend",
          imagen: "./Harold.jpeg"
        },
        {
          codigo: 4,
          nombre: "William Nicolás Buitrago Camacho",
          descripcion:"Estudiante de ingeniería de sistemas en la Universidad Distrital Francisco José de Cladas en la ciudad de Bogotá. Apasionado por la tecnología y por aprender cada día más y más.",
          rol: "Desarrollador Backend",
          imagen: "./Nicolas.jpg"
        },
        {
          codigo: 5,
          nombre: "Hernan Santiago Salamanca Martinez",
          descripcion:"Ingeniero civil. con interés en convertir ciudades por medio de aplicaciones de movilidad sostenible y proyectos tecnologicos que faciliten la vida.",
          rol: "Desarrollador Backend",
          imagen: "./santiago.jpg"
        }
      ],
    };
    
  }

}

</script>

