<template>
  <div>
    <h1 style="color:blue">{{comic.titulo}}</h1>
     <h3>{{comic.descripcion}}</h3>
    <h3 :class="{
        rojo:comic.year <= 2000,
        verde: comic.year > 2000
    }">
        {{comic.year}}
        </h3>
    <img :src="comic.imagen" :title="comic.titulo"/>
    <button @click="seleccionarFavorito()">Seleccionar comic favorito</button>
    <button @click="eliminarComic()">Eliminar comic</button>
  </div>
</template>

<script>
export default {
name:"HijoComic",
props:["comic","index"],
methods:{
    seleccionarFavorito(){
        //metodo para llamara al padre y enviar nuestro click
        this.$emit("seleccionarFavorito",this.comic);
    },
    eliminarComic(){
        this.$emit("eliminarComic",this.index);
    }
}
}
</script>

<style scoped>

</style>