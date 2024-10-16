<!-- 1.- Mostrar Información Básica con Props
Crea un componente Tarjeta que reciba como props el nombre y la descripción de un artículo, y muéstralos dentro de una tarjeta. -->

<template>
  <div class="card my-3" style="width: 18rem;">
    <div class="card-header fw-bold">
      {{ nombre }}
    </div>
    <ul class="list-group list-group-flush">
      <li class="list-group-item">{{ descripcion }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Tarjeta',
  props: {
    nombre: String,
    descripcion: String,
  },
  data() {
    return {};
  }
};
</script>

<style scoped>
</style>