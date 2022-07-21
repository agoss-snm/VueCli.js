<template>
  <div>
    <button @click="$emit('changeFlagFromMain')"> Salir </button>
    <h1>Lista</h1>

     <b-card v-for="(item, i) in Prod" :key="i"
    img-src="https://picsum.photos/600/300/?image=25"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
  <b-card-tittle>{{item.nombre}}</b-card-tittle>
    <b-card-text>
Id: {{item.id}} , Autor: {{item.author}}  Precio: {{item.precio}} </b-card-text>

    <b-button href="#" variant="primary">Comprar</b-button>
  </b-card>

    
  </div>
</template>

<script>
export default {
  name: 'MainPage',
  props:{
    Prod:Object
  },
  
  mounted:function(){
//cuando ya cargo el html

  },
  data(){
    return{

    }
  },
  methods:{

  },
  computed:{

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3{
    text-align: center;
    padding: 5px;
}
</style>
