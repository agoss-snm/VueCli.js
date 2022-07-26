<template>
  <div id="app">
    <LoginUsers v-if="!canAccess" @changeFlag='recibiElMensaje'/>
    <CarritoCompras/>
    <MainPage  v-if="canAccess" @changeFlagFromMain='recibiElMensaje' :Prod='Prod'/>
    <FormularioWeb/>
  </div>
</template>

<script>
import LoginUsers from './components/LoginUsers.vue'
import MainPage from './components/MainPage.vue'
import CarritoCompras from './components/CarritoCompras.vue'
import FormularioWeb from './components/FormularioWeb.vue'

export default {
  name: 'App',
  components: {
    LoginUsers,
    MainPage,
    CarritoCompras,
    FormularioWeb
    
  },
  data(){
    return{
      canAccess: false,
      Prod:[
            {
                'nombre': 'DarkTrhone',
                'id': '54645',
                'author':'ag78t',
                'precio': '389.23'
            },
            {
                'nombre': 'DarkTrhone2',
                'id': '54645',
                'author':'ag78t',
                'precio': '389.23'
            },
            {
                'nombre': 'DarkTrhone3',
                'id': '54645',
                'author':'ag78t',
                'precio': '389.23'
            },
        ],
    }
  },
  methods:{
    recibiElMensaje(){
      this.canAccess= !this.canAccess
    },
    
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
  margin-top: 0px;
}
</style>
