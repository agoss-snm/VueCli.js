<template>
  <div>
    <img alt="logo" src="../assets/logo2.png" width="200px">
    <div class="container">
    <form action="">
      <div class="row">
        <div class="col col-12">
          <br><br>
          <label for="inputNombre" class="text-start">Tu nombre</label>
          <input type="text" class="form-control" id="inputNombre" placeholder="Nombre completo" v-model="name">
          <p>Valida tu nombre: <span class="strong">{{name}}</span></p>
          <br>
          <label for="inputEdad" class="form-label text-start">Edad</label>
          <input type="number" class="form-control" id="inputEdad" placeholder="Edad" v-model.number="edad">
          <br>
          <p>Edad ingresada: <span class="strong">{{edad}}</span></p>
          <label for="inputEmail" class="form-label text-start">Email</label>
          <input type="email" class="form-control" id="inputEmail" placeholder="tu@email.com">
          <br>
          <div class="row">
            <h4>Selecciona tus intereses</h4>
            <div class="col col-2">
              <div class="form-check">
                <input class="form-check-input" type="checkbox" value="vender" id="checkJS" v-model="check">
                <label class="form-check-label" for="checkJS">
                  Vender NTF
                </label>
              </div>
              <div class="form-check">
                <input class="form-check-input" type="checkbox" value="comprar" id="checkReact" v-model="check">
                <label class="form-check-label" for="checkReact">
                  Comprar NTF
                </label>
              </div>
              <div class="form-check">
                <input class="form-check-input" type="checkbox" value="compraryvender" id="checkNg" v-model="check">
                <label class="form-check-label text-start" for="checkNg">
                  Comprar y Vender NTF
                </label>
              
              </div>
            </div>
          </div>
           
          <p>Intereses seleccionados: <span class="strong">{{check}}</span></p>
          <br><br>
<h4>Selecciona tu Pais</h4>
            <select class="form-select"
            aria-label="Default select example"
            v-model="pais">
            
            <option selected></option>
            <option value="Argentina">Argentina</option>
            <option value="Chile">Chile</option>
            <option value="Mexico">Mexico</option>
            <option value="Peru">Peru</option>
            <option value="Uruguay">Uruguay</option>
            
            </select>
    <br>
    <p>Pais Seleccionado: <span class="strong">{{pais}}</span></p>

          <label for="areaComentarios" class="form-label text-start">Comentarios</label>
          <textarea class="form-control" id="areaComentarios" rows="3"></textarea>
          <br>
          <div class="row">
            <h4>Tipo de documento</h4>
            <div class="col">
              <input type="radio" name="checkDNI" class="form-check-input">
              <label for="checkDNI">DNI</label>
            </div>
            <div class="col">
              <input type="radio" name="checkPass" class="form-check-input">
              <label for="checkDNI">Pasaporte</label>
            </div>
            <div class="col">
              <input type="radio" name="checkVisa" class="form-check-input">
              <label for="checkDNI">VISA</label>
            </div>
          </div>
          <hr>
          <div class="row">
            <br>
            <div class="col-10"></div>
            <br>
            <div class="col-2">
              <input type="submit" class="btn btn-primary" value="ENVIAR">
            </div>
            <br>
          </div>
        </div>
      </div>
    </form>
  </div>
  </div>
</template>

<script>
export default {
  name: 'FormularioWeb',
  props:{
  },
  
  mounted:function(){
//cuando ya cargo el html

  },
  data(){
    return{
        name:'',
        check:[],
        pais:'',
        edad:''
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
.strong{
    color:green;
    background-color: beige;
}
</style>