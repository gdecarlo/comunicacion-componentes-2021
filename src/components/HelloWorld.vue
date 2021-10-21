<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ suma }}</h1>
     <button @click="sumar">Sumar</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    titulo:String
  },
  data() {
    return {
      miTitulo: this.titulo,
      suma:0
    }
  },
  methods: {
    sumar(){
      this.suma += 1
    }
  },
  watch:{
    suma(valor){
       if(valor == 3){
         this.$emit("avisar")
       } 
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
