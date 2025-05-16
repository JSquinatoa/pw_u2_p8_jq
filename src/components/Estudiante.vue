<template>
    <div class="container">
        <form >
            <label for="id_nombre">Nombre: </label>
            <input id="id_nombre" type="text" v-model="nuevoNombre">
            {{nuevoNombre}}<br/>
            <label for="id_apellido">Apellido: </label>
            <input id="id_apellido" type="text" v-model="nuevoApellido">
            {{nuevoApellido}}<br>
            <label for="id_edad">Edad: </label>
            <input id="id_edad" type="number" v-model="nuevaEdad">
            {{nuevaEdad}}<br>
            <label for="id_genero">Género: </label>
            <input id="id_genero" type="text" v-model="nuevoGenero">
            {{nuevoGenero}}<br>
            <label for="id_telefono">Teléfono: </label>
            <input id="id_telefono" type="text" v-model="nuevoTelefono">
            {{nuevoTelefono}}<br>
            <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
        </form>
        <ul>
            <li v-for="{nombre, apellido, edad, genero, telefono} in lista" :key="nombre"> Nombre: {{nombre}} - Apellido: {{apellido}} - edad: {{ edad }} - género: {{ genero }} - teléfono: {{ telefono }}</li>
        </ul>
    </div>  
</template>

<script>
export default {
    data(){
        return{
            nuevoNombre: '',
            nuevoApellido: '',
            nuevaEdad: 0,
            nuevoGenero: '',
            nuevoTelefono: '',
            lista: [
                {nombre:"John", apellido:"Quinatoa", edad:23, genero: "masculino", telefono:"09987215076"},
                {nombre:"Steven", apellido:"Guerrero", edad:23, genero: "masculino", telefono:"0995369874"},
                {nombre:"Naidelin", apellido:"Tabango", edad:21, genero: "femenino", telefono:"0991239856"},
                {nombre:"Brigith", apellido:"Mañay", edad:21, genero: "femenino", telefono:"0991567894"},
                {nombre:"Carmen", apellido:"Guerrero", edad:40, genero: "femenino", telefono:"09914562369"},
                {nombre:"Maria", apellido:"Puetate", edad:40, genero: "femenino", telefono:"0991234785"},
                {nombre:"Marco", apellido:"Quinatoa", edad:45, genero: "masculino", telefono:"0991985632"},
            ]
        }
    },
    methods:{
        agregarEstudiante(){
            const nuevo = {
                nombre: this.nuevoNombre,
                apellido: this.nuevoApellido,
                edad: this.nuevaEdad,
                genero: this.nuevoGenero,
                telefono: this.nuevoTelefono
            }
            /* this.lista.unshift(nuevo); */
            this.lista.push(nuevo);
            
        }
    }
}
</script>

<style>

</style>