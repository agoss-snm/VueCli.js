<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <AlumnoLista :Alum="Alum"/>
  </div>
</template>

<script>
import AlumnoLista from './components/AlumnoLista.vue'

export default {
  name: 'App',
  components: {
    AlumnoLista,
    
  },
  data(){
    return{
      Alum:[
            {
                'nombre': 'Jose',
                'apellido': 'Piccioni',
                'edad': '39',
                'nota': '7'
            },
            {
                'nombre': 'Fernando',
                'apellido': 'Rivero',
                'edad': '30',
                'nota': '3'
            },
            {
                'nombre': 'Gissella',
                'apellido': 'Gastin',
                'edad': '32',
                'nota': '10'
            },
        ],
    }
  },
  methods:{
    
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
