<template>
  <div>
    <h1>Hijo: {{numero}}</h1>
    <button @click="sumarDatos">Sumar</button>
    
  </div>
</template>

<script>
export default {
name:"HijoNumero",
props:["numero"],
methods:{
    sumarDatos(){
        this.$emit("sumarNumero", this.numero)
    }
}
}
</script>

<style>

</style>