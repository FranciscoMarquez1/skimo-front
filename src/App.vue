<template>
  <b-container fluid id="app">
    <b-row>
       <NavBar />
    </b-row>
    <b-row class="main-content">
      <b-col cols=8>
        <Clientes-frecuentes />
      </b-col>
      <b-col>
        <Nosotros />
      </b-col>
    </b-row>
    <Footer />
  </b-container>
</template>

<script>
import ClientesFrecuentes from "./components/ClientesFrecuentes.vue";
import Footer from "./components/Footer.vue";
import NavBar from "./components/NavBar.vue";
import Nosotros from "./components/Nosotros.vue";

export default {
  name: "App",
  components: {
    ClientesFrecuentes,
    Footer,
    NavBar,
    Nosotros,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.main-content {
  margin-top: 20px;
}
</style>
