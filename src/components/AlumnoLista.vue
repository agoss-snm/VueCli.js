<template>
  <div>
<table>
                <thead>
                    <tr>
                        <td>Nombre</td>
                        <td>Apellido</td>
                        <td>Edad</td>
                        <td>Nota</td>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(item, i) in Alum" :key="i" :class='{"aprobado":item.nota>=7, "desaprobado":item.nota<7} '>
                        <td>{{item.nombre}}</td>
                        <td>{{item.apellido}}</td>
                        <td>{{item.edad}}</td>
                        <td>{{item.nota}}</td>
                    </tr>
                </tbody>
            </table>
  </div>
</template>

<script>
export default {
  name: 'AlumnoLista',
  props:{
    Alum:Object
  },
  
  mounted(){

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
button{
    text-align: center;
    color: rgb(219, 219, 219);
    background: #1f2335;
    border: none;
    height: 40px;
    font-size: 14px;
    border-radius: 50px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.4) ;
    left: 50%;
    padding: 0 10px;
    
}
.container{
    text-align: center;
}
table{
    text-align: center;
    align-items: center;
    margin-left: auto;
    margin-right: auto;
}
p{
    font-size: 40px;
    color: #1f2335;
    border: medium double #1f2335;}
h1{
    color: rgb(17, 150, 61);
    font-size: clamp(2.5rem, 8vw, 6rem);
    text-align: center;
    letter-spacing: -0.02em;
    width: 100%;
    display: block;
    line-height: 0.95;
}

.aprobado{
    background-color: rgb(65, 141, 65);
}


.desaprobado{
    background-color: rgb(189, 119, 15);
}

nav{
    background-color: rgb(31, 31, 31);
    color: white;
    align-items: center;
    text-align: center;
    height: 10vh;

    
}
li{
    list-style: none;
    display: inline;
    padding: 100px;
    font-size: 30px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
</style>
