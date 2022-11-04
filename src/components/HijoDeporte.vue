<template>
  <div>
    <h2 style="color:blue">
        {{nombredeporte}}
    </h2>
    <button @click="selecionarFavorito">Select favorito</button>
  </div>
</template>

<script>
export default {
name:"HijoDeporte",
props:["nombredeporte"],
methods:{
    selecionarFavorito(){
        //cuando pilsemos en el hijo, llamamos al metodo 
        //del padre que nos han enviado por props
        //paramentros van en parentesis separado por comas
        this.$emit("seleccionarFavoritoParent","Su favorito es " + this.nombredeporte);
    }
},
mounted(){
    console.log(this.nombredeporte)
}
}
</script>

<style>

</style>