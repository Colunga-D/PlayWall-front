<template>
    <div class="contact-page">
      <div class="background-image"></div>
      <div class="contact-container">
        <h2 class="contact-title">Contacto</h2>
        <div class="contact-info">
          <div class="contact-item">
            <h3 class="contact-item-title">Correo Electrónico</h3>
            <p class="contact-item-content">PlayWall@gmail.com</p>
          </div>
          <div class="contact-item">
            <h3 class="contact-item-title">Teléfono</h3>
            <p class="contact-item-content">123-456-789</p>
          </div>
          <div class="contact-item">
            <h3 class="contact-item-title">Dirección</h3>
            <p class="contact-item-content">Calle xxx, Gijón, Asturias</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    
  };
  </script>
  
  <style scoped>
  .contact-page {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .background-image {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('/path/to/your/image.jpg'); 
    background-size: cover;
    filter: brightness(0.5); 
    z-index: -1;
  }
  
  .contact-container {
    max-width: 800px; 
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.1);
    background-color: rgba(255, 255, 255, 0.9); 
  }
  
  .contact-title {
    font-size: 2.5rem; 
    margin-bottom: 20px;
    text-align: center;
    color: #333333;
  }
  
  .contact-info {
    display: flex;
    flex-direction: column;
  }
  
  .contact-item {
    margin-bottom: 20px;
  }
  
  .contact-item-title {
    font-size: 1.8rem; 
    margin-bottom: 10px;
    color: #007bff; 
  }
  
  .contact-item-content {
    font-size: 1.2rem; 
    color: #555555; 
  }
  </style>