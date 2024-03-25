<template>
    <div class="image-info-container" :style="{ backgroundImage: `url(${backgroundImage})` }">
      <div class="image-container">
        <img :src="imageSrc" alt="Imagen" class="main-image">
      </div>
      <div class="info-container">
        <h2>{{ title }}</h2>
        <div class="info">
          <div class="info-item">
            <span class="info-label">Sitio:</span>
            <span>{{ place }}</span>
          </div>
          <div class="info-item">
            <span class="info-label">Hora:</span>
            <span>{{ time }}</span>
          </div>
          <div class="info-item">
            <span class="info-label">Modalidad:</span>
            <span>{{ mode }}</span>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      imageSrc: String,
      title: String,
      place: String,
      time: String,
      mode: String,
      backgroundImage: {
        type: String,
        default: '/default-background.jpg' 
      }
    }
  };
  </script>
  
  <style scoped>
  .image-info-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-size: cover;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    height: 90vh;
  }
  
  .image-container {
    width: 500px;
    height: 300px;
    overflow: hidden;
    border: 2px solid #ccc; /* Borde alrededor de la imagen */
    border-radius: 10px;
  }
  
  .main-image {
    width: 100%;
    height: auto;
  }
  
  .info-container {
    flex: 1;
    padding: 20px;
    background-color: rgba(243, 239, 239, 0.8); /* Color de fondo del contenedor de información */
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  h2 {
    margin-bottom: 10px;
    font-size: 1.5rem;
    color: #333;
    transition: color 0.3s ease;
  }
  
  h2:hover {
    color: #007bff;
  }
  
  .info {
    display: flex;
    flex-direction: column;
  }
  
  .info-item {
    margin-bottom: 10px;
  }
  
  .info-label {
    font-weight: bold;
  }
  </style>