<template>
  <!-- <PadreDeporte/> -->
 <!--  <PadreNumero/>  -->
 <!-- <PadreComics/> -->
 <MenuComponent/>
 <router-view></router-view>
</template>

<script>
// import PadreDeporte from './components/PadreDeporte.vue'
//import PadreNumero from './components/PadreNumero.vue'
// import PadreComics from './components/PadreComics.vue'
import MenuComponent from './components/MenuComponent.vue'
export default {
  name: 'App',
  components: {
    // PadreDeporte,
    //PadreNumero
    // PadreComics
    MenuComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
