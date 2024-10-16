<!-- 2.- Pasar Props con Números
Crea un componente Producto que reciba el nombre y precio de un producto como props y muestre la información en un formato legible. -->
<template>
  <div class="card my-3" style="width: 18rem;">
    <div class="card-header fw-bold">
      {{ nombre }}
    </div>
    <ul class="list-group list-group-flush">
      <li class="list-group-item">${{ precio }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Actividad2',
  props:{
    nombre: String,
    precio: Number,
  },
  data() {
    return {

    };
  }
};
</script>

<style scoped>
</style>