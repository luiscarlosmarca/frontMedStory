<template>
  <div class="container-fluid" id="app">
    <form v-on:submit.prvent="guardarPaciente" method="POST">
      <h1 align="center">Creacion de pacientes</h1>
      <h2 align="center">MedStory</h2>
       <div class="form-group">
        <label> Nombre del paciente</label>
        <input class="form-control" v-model="nombre">
      </div>
      <div class="form-group">
              <label> Cedula</label>
              <input type='text' class="form-control" v-model="cedula"/>
                               
        </div>
       <div class="form-group">
        <label> EPS</label>
         <select v-model="eps">
          <option value="volvo">Salud vida</option>
          <option value="saab">Cafe salud</option>
          <option value="mercedes">SURA</option>
          <option value="audi">Nueva Eps</option>
        </select> 
      </div>
      <div class="form-group">
              <label> Fecha de nacimiento</label>
              <input type='date' class="form-control" v-model="fena"/>
                               
        </div>
      <div class="form-group">
        <label> Clasificacion</label>
         <select v-model="eps">
          <option value="volvo">Diabetico</option>
          <option value="saab">Hipertenso</option>
          <option value="mercedes">Saludable</option>
          <option value="audi">Atletico</option>
        </select> 
      </div>
         
      <div class="form-group">
        <button class="btn btn-dark" type="submit">Guardar Paciente</button>
      </div>
       

    </form>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      paciente:[nombre,cedula,fena,eps,clasificacion],
      error:[],
     
    }
  },
  methods: {
   guardarPaciente:function(){
     var url=http//:localhost.com:8080/api/v1/pacientes';
     axios.post(url,{
       paciente:this.paciente
     }).then(response=>{
       console.log("200")
     }).catch(error=>{
       this.error=error.response.data
     })
   }
  },
}
</script>
import axios from 'axios';
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
