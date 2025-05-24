<template>
 <!-- <HolaMundoView/> -->
 <!-- <ContadorView/> -->
 <!-- <EstudianteView/> -->
 <!-- <EstudianteTablaView/> -->
<!-- <FormularioLibroView/> -->
<!--   <PreguntaView/> -->  
   <ClimaView/>


</template>

<script>
import HolaMundoView from "../src/views/HolaMundoView.vue"
import ContadorView from "./views/ContadorView.vue"
import EstudianteView from "@/views/EstudianteView.vue"
import EstudianteTablaView from "@/views/EstudianteTablaView.vue"
import FormularioLibroView from "@/views/FormularioLibroView.vue"
import PreguntaView from "@/views/PreguntaView.vue"
import ClimaView from "@/views/ClimaView.vue"
export default {
  name: 'App',
  components: {
    HolaMundoView,
    ContadorView,
    EstudianteView,
    EstudianteTablaView,
    FormularioLibroView,
    PreguntaView,
    ClimaView
  }
}
</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
</style>