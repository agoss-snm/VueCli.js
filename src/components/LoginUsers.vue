<template>
  <div>
  <b-navbar type="dark" variant="dark"  >
    <b-navbar-brand href="#" >NFT-Store</b-navbar-brand>
    

  </b-navbar>


  <h1>Login</h1>
  <label for="nombre">Name</label>
  <input type="text" name="name" v-model="nombre"/>
  <label for="password">Pass</label>
   <input type="password" name="password" v-model="password"/>
   <button @click="cambiarValor">Go</button>
</div>
</template>

<script>

export default {
  name: 'LoginUsers',
  props:{
    Alum:Object
  },
  
  mounted(){

  },
  data(){
    return{
        nombre:'',
        password:''
    }
  },
  methods:{
    cambiarValor(){
        if (this.nombre == "admin" && this.password == "1234"){
            this.$emit('changeFlag')
        }
    }
  },
  computed:{

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3{
    text-align: right;
    padding: 5px;
}
.navbar-expand{
justify-content: space-between;
}
</style>
