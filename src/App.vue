<template>
  <div id="app">
    <h1>RELATÓRIO</h1>
    <ExAlunos />
  </div>

</template>
<script>
import ExAlunos from './components/ExAlunos.vue'
export default {
  name: 'app',
  components: {
    ExAlunos
  }
}
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  font-family: 'Optima', sans-serif;
  width: 1000px;
  text-align:center;
  color:rgb(13, 3, 56);
}

</style>