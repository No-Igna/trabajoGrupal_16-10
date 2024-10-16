<!-- 3.- Controlar el Tipo de Prop
Crea un componente Avatar que reciba como prop la URL de una imagen de perfil y el tamaño de la imagen (en píxeles). Asegúrate de que el tamaño sea de tipo Number. -->
<template> 
    <img :src="url" class="card-img-top" :style="{width:tamano+'px'}" alt="">
</template>

<script>
export default {
  name: 'Actividad3',
  props:{
    url:String,
    tamano:Number,
  },
  data() {
    return {};
  }
};
</script>

<style scoped>
</style>