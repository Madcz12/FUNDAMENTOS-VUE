<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <strong>
      VIVA VUE!!!
    </strong>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  created() { console.log("created - Hola Mundo") },
  beforeMount() { console.log("beforeMount - Hola Mundo") },
  mounted() { console.log("mounted - Hola Mundo") },
  beforeUpdate() { console.log("beforeUpdate - Hola Mundo") },
  updated() { console.log("updated - Hola Mundo") },
  activated() { console.log("activated - Hola Mundo") },
  deactivated() { console.log("deactivated - Hola Mundo") },
  beforeUnmount() { console.log("beforeUnmount - Hola Mundo") },
  unmounted() { console.log("unmounted - Hola Mundo") },
  errorCaptuted() { console.log("errorCaptured - Hola Mundo") },
  renderTracked() { console.log("renderTracked - Hola Mundo") },
  renderTriggered() { console.log("renderTriggered - Hola Mundo") },

  props: { // propiedades
    msg: String,
  },
  data() { // funcion que retorna un objeto
    return {
      // retorna un objeto
      PrimeraPropiedad: "Miguel"
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: blue;
}

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
