<template>
    <div class="soccer-banner" :style="{ backgroundImage: 'url(' + backgroundImage + ')' }">
      
    </div>
  </template>
  
  <script>
  export default {
    props: {
      backgroundImage: {
        type: String,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  .soccer-banner {
    width: 100%;
    height:450px; 
    background-size: cover;
    background-position: center;
    
    box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.3);
  }
  </style>