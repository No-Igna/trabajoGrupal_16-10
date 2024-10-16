<!-- 4.-  Pasar Objetos como Props
Crea un componente Usuario que reciba como prop un objeto con la información de un usuario (nombre, apellido, edad) y muéstrelo en un formato de tarjeta. -->
<template>
  <div class="card my-3" style="width: 18rem;">
    <div class="card-body">
      <h5 class="card-title">{{nombre}} {{ apellido }}</h5>
      <p class="card-text">edad: {{ edad }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Usuario',
  props: {
    nombre: String,
    apellido: String,
    edad: Number,
  },
  data() {
    return {};
  }
};
</script>

<style scoped></style>