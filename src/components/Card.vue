<template>
  <div class="card">
    <div class="card-content">
      <div class="image-container">
        <div class="vertical-center">
          <img :src="cardData['Imagen oficial']" alt="Card Image" />
        </div>
      </div>
      <div class="card-details">
        <p>ID Subasta: {{ cardData["ID Subasta"] }}</p>
          <p>Codigo carta: {{ cardData["Codigo carta"] }}</p>
          <p>Rareza: {{ cardData["Rareza"] }}</p>
          <p>Oferta: {{ cardData["Oferta"] }}</p>
          <p>Inicio: {{ cardData["Inicio"] }}</p>
          <p>Fin: {{ cardData["Fin"] }}</p>
          <p>Precio Base: {{ cardData["Precio Base"] }}</p>
          <p>Precio Mercado: {{ cardData["Precio Mercado"] }}</p>
          <p>Venta: {{ cardData["Venta"] ? "Sí" : "No" }}</p>
          <p>Ciudad: {{ cardData["Ciudad"] }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, type PropType } from 'vue';

export default defineComponent({
  props: {
    cardData: {
      type: Object as PropType<any>,
      required: true,
    },
  },
});
</script>

<style scoped>
.card {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
}

.card-content {
  display: flex;
  height: auto; 
}

.image-container {
  flex: 1;
  padding-right: 10px;
  display: flex;
  justify-content: center; 
  align-items: center; 
  max-height: 100%; 
}

.vertical-center {
  text-align: center; 
}

.card-header {
  font-weight: bold;
}

img {
  max-height: 100%; 
  max-width: 100%; 
  margin-bottom: 10px;
}
</style>
