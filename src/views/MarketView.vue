<template>
    <div class="auction-view">
      <h1>Auction View</h1>
      <div class="card-grid">
        <div v-for="auction in auctions" :key="auction['ID Subasta']" class="card-item">
          <Card :cardData="auction" class="card-container" />
        </div>
      </div>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent } from 'vue';
  import Card from '@/components/Card.vue';
  
  export default defineComponent({
    components: {
      Card,
    },
    data() {
      return {
        auctions: [
        {
            "ID Subasta": 1,
            "Nombre cara": "Sample Card 1",
            "Codigo carta": "12345",
            "Rareza": "Rare",
            "Oferta": 100,
            "Inicio": "2023-11-01",
            "Fin": "2023-11-10",
            "Precio Base": 50,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card1_upload.jpg",
            "Precio Mercado": 150,
            "Venta": true,
            "Ciudad": "Sample City 1"
          },
          {
            "ID Subasta": 2,
            "Nombre cara": "Sample Card 2",
            "Codigo carta": "67890",
            "Rareza": "Common",
            "Oferta": 75,
            "Inicio": "2023-11-05",
            "Fin": "2023-11-15",
            "Precio Base": 30,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card2_upload.jpg",
            "Precio Mercado": 90,
            "Venta": false,
            "Ciudad": "Sample City 2"
          },
          {
            "ID Subasta": 3,
            "Nombre cara": "Sample Card 3",
            "Codigo carta": "13579",
            "Rareza": "Ultra Rare",
            "Oferta": 120,
            "Inicio": "2023-11-10",
            "Fin": "2023-11-20",
            "Precio Base": 50,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card3_upload.jpg",
            "Precio Mercado": 200,
            "Venta": true,
            "Ciudad": "Sample City 3"
            },
            {
            "ID Subasta": 1,
            "Nombre cara": "Sample Card 1",
            "Codigo carta": "12345",
            "Rareza": "Rare",
            "Oferta": 100,
            "Inicio": "2023-11-01",
            "Fin": "2023-11-10",
            "Precio Base": 50,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card1_upload.jpg",
            "Precio Mercado": 150,
            "Venta": true,
            "Ciudad": "Sample City 1"
          },
          {
            "ID Subasta": 2,
            "Nombre cara": "Sample Card 2",
            "Codigo carta": "67890",
            "Rareza": "Common",
            "Oferta": 75,
            "Inicio": "2023-11-05",
            "Fin": "2023-11-15",
            "Precio Base": 30,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card2_upload.jpg",
            "Precio Mercado": 90,
            "Venta": false,
            "Ciudad": "Sample City 2"
          },
          {
            "ID Subasta": 3,
            "Nombre cara": "Sample Card 3",
            "Codigo carta": "13579",
            "Rareza": "Ultra Rare",
            "Oferta": 120,
            "Inicio": "2023-11-10",
            "Fin": "2023-11-20",
            "Precio Base": 50,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card3_upload.jpg",
            "Precio Mercado": 200,
            "Venta": true,
            "Ciudad": "Sample City 3"
            },
            {
            "ID Subasta": 1,
            "Nombre cara": "Sample Card 1",
            "Codigo carta": "12345",
            "Rareza": "Rare",
            "Oferta": 100,
            "Inicio": "2023-11-01",
            "Fin": "2023-11-10",
            "Precio Base": 50,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card1_upload.jpg",
            "Precio Mercado": 150,
            "Venta": true,
            "Ciudad": "Sample City 1"
          },
          {
            "ID Subasta": 2,
            "Nombre cara": "Sample Card 2",
            "Codigo carta": "67890",
            "Rareza": "Common",
            "Oferta": 75,
            "Inicio": "2023-11-05",
            "Fin": "2023-11-15",
            "Precio Base": 30,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card2_upload.jpg",
            "Precio Mercado": 90,
            "Venta": false,
            "Ciudad": "Sample City 2"
          },
          {
            "ID Subasta": 3,
            "Nombre cara": "Sample Card 3",
            "Codigo carta": "13579",
            "Rareza": "Ultra Rare",
            "Oferta": 120,
            "Inicio": "2023-11-10",
            "Fin": "2023-11-20",
            "Precio Base": 50,
            "Imagen oficial": "https://youre.outof.games/media/uploads/56/3b/563b42d2-f019-47bc-9513-26686a790bfc/8715625.jpg",
            "Imagen subida": "https://example.com/card3_upload.jpg",
            "Precio Mercado": 200,
            "Venta": true,
            "Ciudad": "Sample City 3"
            }
        ],
      };
    },
  });
  </script>
  
  <style scoped>
  .auction-view {
  }
  
  .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    grid-gap: 30px;
    max-width: 100%;
  }
  
  .card-item {
    border: 1px solid #ccc; 
    border-radius: 8px; 
    padding: 10px; 
}
  
  .card-container {
    border: 0px;
  }
  
  </style>
  
  