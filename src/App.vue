<template>
 <!-- <HolaMundoView/> -->
 <!-- <ContadorView/> -->
 <!-- <EstudianteView/> -->
 <!-- <EstudianteTablaView/> -->
  <FormularioLibroView/>

</template>

<script>
import HolaMundoView from "../src/views/HolaMundoView.vue"
import ContadorView from "./views/ContadorView.vue"
import EstudianteView from "@/views/EstudianteView.vue"
import EstudianteTablaView from "@/views/EstudianteTablaView.vue"
import FormularioLibroView from "@/views/FormularioLibroView.vue"
export default {
  name: 'App',
  components: {
    HolaMundoView,
    ContadorView,
    EstudianteView,
    EstudianteTablaView,
    FormularioLibroView
  }
}
</script>

<style scoped>

</style>