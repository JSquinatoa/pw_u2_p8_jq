<template>
    <div class="container">
        <h1>Contador</h1>
        <p> {{this.numero}}<sup>2</sup> = {{calCuadrado}} </p>
        <section>
            <button v-on:click="incrementar()">+ 1</button>
            <button v-on:click="decrementar()">- 1</button>
        </section>


        <!-- <p>{{numero + 1}}</p>        
        <p>{{texto}}</p>        
        <p>{{activo}}</p>        
        <p>{{usuario}}</p>        
        <p>{{arreglo}}</p>        
        {{1+1}}
        1+1
        {{true?'es verdadero': 'es Falso'}} 
        true?'es verdadero': 'es Falso' -->
    </div>
</template>

<script>
export default {
    data() {
        return{
            numero: 5,
            texto: 'John Quinatoa',
            activo: true,
            usuario:{
                nombre:"John Quinatoa",
                edad: 23,
                genero: "masculino"
            },
            arreglo:["Amarillo", "Azul"]
        };
    },

    methods:{
        calcularCuadrado() {
            console.log("Entro al método");            
            return this.numero*this.numero            
        },
        incrementar(){
            this.numero++
        },
        decrementar(){
            this.numero--
        }
    },

    computed:{
        calCuadrado(){
            console.log("Entro propiedad computada");            
            return this.numero*this.numero               
        }
    }

}
</script>

<style>

</style>