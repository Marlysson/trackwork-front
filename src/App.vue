<template>
  <div id="app">
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: 'App',

  mounted(){
    axios.get("http://localhost:8000/api/projects").then(function(response){
      console.log(response)
    }).catch(function(error){
      console.log(error);
    })

    axios.post("http://localhost:8000/api/projects", {"name": "novo projeto"}).then(function(response){
      console.log(response)
    }).catch(function(error){
      console.log(error);
    })
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
