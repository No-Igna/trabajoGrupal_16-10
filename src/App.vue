<script>
import Tarjeta from './components/Tarjeta.vue';
import Producto from './components/Producto.vue';
import Avatar from './components/Avatar.vue';
import Usuario from './components/Usuario.vue';
import EstadoPedido from './components/EstadoPedido.vue'

export default {
  name: 'App',
  components: {
    Tarjeta, Producto, Avatar, Usuario, EstadoPedido,
  },
  data() {
    return{
      user: [{
        nombre: 'José Ignacio',
        apellido: 'Pérez',
        edad: 27
      },
      {
        nombre: 'Lore',
        apellido: 'Alarcón',
        edad: ''
      }],
    }
  }
};
</script>

<template>
  <div class="container">
    <Tarjeta :nombre="'Instrumento de practica 1'"
      :descripcion="'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus impedit voluptatem nobis, neque atque nemo maxime incidunt ex consequatur ad odit et obcaecati, ipsam veniam aspernatur delectus libero nisi nam.'" />
    <Producto :nombre="'Instrumento de practica 2'" :precio="1000" />
    <Avatar :url="'https://i.pinimg.com/736x/0d/d5/66/0dd56675bbc4e8658012d5997ee985ac.jpg'" :tamano="100" />
    <div v-for="persona in user">
      <Usuario :nombre="persona.nombre" :apellido="persona.apellido" :edad="persona.edad"/>
    </div>
    <EstadoPedido :estado="'enviado'" />
    <EstadoPedido :estado="'pendiente'" />
    <EstadoPedido :estado="'cancelado'" />
    <EstadoPedido :estado="'otro'" />

  </div>
</template>

<style scoped></style>
