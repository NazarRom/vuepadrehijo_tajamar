<template>
  <div>
    <h1>
        Padre Numero
    </h1>
    <h2>{{suma}}</h2>
    <button @click="crearNumero">Crear</button>
    <ul>
        <li v-for="n in numeros" :key="n">
            <HijoNumero :numero="n" v-on:sumarNumero="sumarNumero"/>
        </li>
        </ul>
  </div>
</template>

<script>
import HijoNumero from './HijoNumero.vue';
export default {
name:"PadreNumero",
components:{
    HijoNumero
},
methods:{
   crearNumero(){
    var random = parseInt(Math.random() * 100);
    this.numeros.push(random);
   },
   sumarNumero(numero){
    this.suma = this.suma + numero;
   }
},
data(){
    return{
        numeros:[],
        suma:0
    }
}
}
</script>

<style>

</style>