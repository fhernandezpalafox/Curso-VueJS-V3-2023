<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />

  <div id="aplicacion">
    <AppIdioma idioma="ingles" />
    <AppIdioma idioma="castellano" />
  </div>

  <br />
  <br />
  <div style="display: flex;justify-content: center;">
    <ArticulosTabla v-bind:datos="datos" />
  </div>
  
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import AppIdioma from "./components/Idioma.vue";
import ArticulosTabla from "./components/Articulos.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    AppIdioma,
    ArticulosTabla,
  },
  data() {
    return {
      datos: [
        {
          codigo: 1,
          descripcion: "papas",
          precio: 12.52,
        },
        {
          codigo: 2,
          descripcion: "naranjas",
          precio: 21,
        },
        {
          codigo: 3,
          descripcion: "peras",
          precio: 18.2,
        },
      ],
    };
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
  margin-top: 60px;
}
</style>
