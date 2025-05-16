<template>
    <div class="container">
        <label for="id_nombre">Nombre: </label>
        <input id="id_nombre" type="text" v-model="nuevoNombre">
        {{nuevoNombre}}
        <label for="id_apellido">Apellido: </label>
        <input id="id_apellido" type="text" v-model="nuevoApellido">
        {{nuevoApellido}}
        <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
        <ul>
            <li v-for="{nombre, apellido} in lista" :key="nombre"> Nombre: {{nombre}} - Apellido: {{apellido}} </li>
        </ul>
    </div>  
</template>

<script>
export default {
    data(){
        return{
            nuevoNombre: '',
            nuevoApellido: '',
            lista: [
                {nombre:"John", apellido:"Quinatoa"},
                {nombre:"Steven", apellido:"Guerrero"},
                {nombre:"Naidelin", apellido:"Tabango"},
                {nombre:"Brigith", apellido:"Mañay"},
                {nombre:"Carmen", apellido:"Guerrero"},
                {nombre:"Maria", apellido:"Puetate"},
                {nombre:"Marco", apellido:"Quinatoa"},
            ]
        }
    },
    methods:{
        agregarEstudiante(){
            const nuevo = {
                nombre: this.nuevoNombre,
                apellido: this.nuevoApellido
            }
            /* this.lista.unshift(nuevo); */
            this.lista.push(nuevo);
            
        }
    }
}
</script>

<style>

</style>