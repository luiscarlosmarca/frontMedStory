<template>
  <div class="container-fluid" id="app">
    <form @Submit.prevent="hi">
      <h1 align="center">Creacion de pacientes</h1>
      <h2 align="center">MedStory</h2>
       <div class="form-group">
        <label> Nombre del paciente</label>
        <input class="form-control" v-model="nombre">
      </div>
      <div class="form-group">
        <button class="btn btn-dark" type="submit">Guardar Paciente</button>
      </div>
       </div>

    </form>
  </div>
</template>

<script>
export default {
  name: 'app'
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
</style>
