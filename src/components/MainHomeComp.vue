<template>
    <main class="home-main">
      <div class="column" @click="navigateTo('soccer')">
        <img src="/path/to/soccer-image.jpg" alt="Soccer" class="column-image">
        <h3 class="column-title">Fútbol</h3>
      </div>
      <div class="column" @click="navigateTo('tennis')">
        <img src="/path/to/tennis-image.jpg" alt="Tennis" class="column-image">
        <h3 class="column-title">Tenis</h3>
      </div>
      <div class="column" @click="navigateTo('basketball')">
        <img src="/path/to/basketball-image.jpg" alt="Basketball" class="column-image">
        <h3 class="column-title">Baloncesto</h3>
      </div>
    </main>
  </template>
  
  <script setup>
  import { useRouter } from 'vue-router';
  
  const router = useRouter();
  
  const navigateTo = (route) => {
    router.push({ name: route });
  };
  </script>
  
  <style scoped>
  .home-main {
    display: flex;
    justify-content: space-between;
  }
  
  .column {
    flex: 1;
    margin: 0 10px;
    text-align: center;
    cursor: pointer;
  }
  
  .column:hover {
    transform: translateY(-5px);
  }
  
  .column-image {
    width: 100%;
    height: auto;
    border-radius: 10px;
    transition: transform 0.3s ease;
  }
  
  .column-title {
    margin-top: 10px;
    font-size: 1.5rem;
    color: #333;
  }
  </style>