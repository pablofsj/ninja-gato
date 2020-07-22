<template>
  <div>
    <div class="row">
      <div class="col m12 s12">
        <h3>Ninja-Gato</h3>
      </div>
    </div>
    <div class="row">
      <div class="col m6 s12">
        <button href="#modal1" @click="mostrarNinja()" class="btn modal-trigger">Mostrar Ninja</button>
      </div>
      <div class="col m6 s12">
        <button href="#modal1" @click="mostrarGato()" class="btn modal-trigger">Mostrar Gato</button>
      </div>
    </div>
    <div class="row">
      <div class="col m12 s12">
        <p><img :src="muestra_imagen"></p>
      </div>
    </div>
  </div>
</template>

<script>
const imagen_ninja = "https://cdn131.picsart.com/314127840156211.png?type=webp&to=min&r=640";
const imagen_gato ="https://i.pinimg.com/originals/1e/64/f7/1e64f76c7a2e6c15e56cdb813854c1e4.jpg"


export default {
  name: 'ShowImage',
  data:function() {
    return {
      muestra_imagen: "https://image.freepik.com/free-icon/interrogation-mark-circle_318-9651.jpg"
    }
  },


  methods: {
    mostrarNinja: function(){
      this.muestra_imagen = imagen_ninja
    },
    mostrarGato: function(){
      this.muestra_imagen = imagen_gato
    }
  },
 
  beforeUpdate() {
    alert(`La imagen será cambiada a ${(this.muestra_imagen == imagen_ninja) ? "ninja" : "gato"} `);
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap');

  h3{
    font-family: 'Fredoka One', cursive;
  }


</style>
