<template>
    <div class="news-container">
      <div v-for="(article, index) in articles" :key="index" class="news-card">
        <img :src="article.image" :alt="article.title" class="news-image">
        <div class="news-content">
          <h3 class="news-title">{{ article.title }}</h3>
          <p class="news-description">{{ article.description }}</p>
          <a :href="article.link" class="read-more">Leer más</a>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        articles: [
          {
            title: "Título de la noticia 1",
            description: "Descripción de la noticia 1",
            image: "/images/news1.jpg",
            link: "/news/news1"
          },
          {
            title: "Título de la noticia 2",
            description: "Descripción de la noticia 2",
            image: "/images/news2.jpg",
            link: "/news/news2"
          },
          
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .news-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    height: 100vh;
  }
  
  .news-card {
    width: 300px;
    margin: 20px;
    padding: 15px;
    border-radius: 10px;
    box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }
  
  .news-card:hover {
    transform: translateY(-5px);
  }
  
  .news-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 10px;
  }
  
  .news-title {
    font-size: 1.5rem;
    margin-bottom: 10px;
  }
  
  .news-description {
    font-size: 1rem;
    margin-bottom: 15px;
  }
  
  .read-more {
    color: #007bff;
    text-decoration: none;
    font-weight: bold;
    transition: color 0.3s ease;
  }
  
  .read-more:hover {
    color: #0056b3;
  }
  </style>