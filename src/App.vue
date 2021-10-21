<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <HelloWorld msg="Otra instancia" :titulo="miTituloEnPadre" @avisar="mostrarAlerta"/>
    <hr>
    <h3 v-if="showAlerta">El nivel llegó a 3</h3>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld: HelloWorld
  },
  data() {
    return {
      miTituloEnPadre:"un titulo",
      showAlerta: false
    }
  },
  methods: {
    mostrarAlerta(){
      this.showAlerta = true
    }
  },
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
