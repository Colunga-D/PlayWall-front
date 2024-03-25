<template>
    <div class="image-info-container">
      <div class="image-container">
        <img :src="imageSrc" alt="Imagen">
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
      mode: String
    }
  };
  </script>
  
  <style scoped>
  .image-info-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-image: url('/path/to/background-image.jpg');
    background-size: cover;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .image-container {
    flex: 1;
    margin-right: 20px;
  }
  
  .image-container img {
    width: 100%;
    height: auto;
    border-radius: 10px;
    transition: transform 0.3s ease;
  }
  
  .image-container img:hover {
    transform: scale(1.05);
  }
  
  .info-container {
    flex: 1;
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