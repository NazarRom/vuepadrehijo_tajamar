<template>
  <div>
    <h1>Padre deporte</h1>
    <h1 v-if="favorito">{{favorito}}</h1>
    <hr/>
    <ul>
        <li v-for="depor in deportes" :key="depor">
            <HijoDeporte :nombredeporte="depor" v-on:seleccionarFavoritoParent="seleccionarFavoritoParent"/>
        </li>
    </ul>
    
  </div>
</template>

<script>
import HijoDeporte from './HijoDeporte.vue';
export default {
  name: "PadreDeortes",
  components:{
    HijoDeporte
  },
   methods:{
    seleccionarFavoritoParent(nombre){
        this.favorito = nombre;
        console.log(nombre)
    }
  },
  data() {
    return {
      deportes: ["Surf", "Curling", "Padel", "Futbol", "Peonza"],
      favorito:null
    };
  },
};
</script>

<style>
</style>