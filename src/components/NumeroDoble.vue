<template>
  <div>
    <h1>Numero doble parámetros</h1>
    <button @click="redirectToHome()">Home</button>
    <h2 style="color: orange" v-if="mensaje">
      {{ mensaje }}
    </h2>
    <div v-else>
      <h2 style="color: blue">El número recibido es : {{ numero }}</h2>
      <h2 style="color: red">El doble es {{ doble }}</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "NumeroDoble",
  methods: {
    redirectToHome() {
      this.$router.push("/");
    },
    mostrarDoble() {
      this.numero = this.$route.params.numero;
      this.doble = parseInt(this.numero) * 2;
    },
  },
  mounted() {
    //debemos capturar los parametros  en este metodo
    if (this.$route.params.numero == "") {
      this.mensaje = "No tenemos parámetros";
    } else {
      this.mostrarDoble();
    }
  },
  data() {
    return {
      mensaje: null,
      numero: 0,
      doble: 0,
    };
  },
  watch: {
    //el control de la variable se realiza
    //mediante STRING y no se utiliza la palabra this
    "$route.params.numero"(nextVal, oldVal) {
      //si ha cambuiado, realizamos las acciones
      if (nextVal != oldVal) {
        //acciones
        this.mostrarDoble();
      }
    },
  },
};
</script>

<style>
</style>