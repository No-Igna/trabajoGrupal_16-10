<!-- 5.-  Renderizado Condicional con Props
Crea un componente EstadoPedido que reciba como prop el estado de un pedido (por ejemplo, "enviado", "pendiente", "cancelado") y muestre un mensaje diferente dependiendo del estado.
DEBEN USAR Bootstrap Y subirlos a un repositorio -->
<template>
  <div class="my-3">
    <div v-if="estado==='enviado'" class="alert alert-success" role="alert">
      <p>el pedido ha sido enviado.</p>
    </div>
    <div v-else-if="estado==='pendiente'" class="alert alert-info" role="alert">
      <p>el envio del pedido aun se encuentra pendiente.</p>
    </div>
    <div v-else-if="estado==='cancelado'" class="alert alert-danger" role="alert">
      <p>El pedido ha sido cancelado</p>
    </div>
    <div v-else class="alert alert-danger" role="alert">
      <p>Estado desconocido</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EstadoPedido',
  props:{
    estado:String
  },
  data() {
    return {};
  }
};
</script>

<style scoped>
</style>