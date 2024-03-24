<template>
    <footer class="sports-footer">
      <div class="footer-content">
        <div class="slogan">
          <h3 class="slogan-text">Play With All</h3>
          <p>Rompe el muro y juega con nuevas personas</p>
        </div>
        <div class="about-section">
          <h4 class="about-title">Sobre PlayWall</h4>
          <hr class="underline">
          <p class="about-text">
            Somos una entidad enfocada en que las personas puedan encontrar gente con la que jugar y poder hacer deporte juntos. Si nunca has podido realizar esa actividad que tanto querías, ahora es tu momento, ¡diviértete!
          </p>
        </div>
        <div class="social-media">
          <h4 class="social-title">Redes Sociales</h4>
          <div class="social-icons">
            <a href="#" class="social-link">
              <img src="/public/images/facebook-icon.png" alt="Facebook">
            </a>
            <a href="#" class="social-link">
              <img src="/public/images/instagram-icon.png" alt="Instagram">
            </a>
            <a href="#" class="social-link">
              <img src="/public/images/google-icon.png" alt="Google">
            </a>
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <style scoped>
  .sports-footer {
    background-color: #1a1a1a;
    color: #fff;
    padding: 30px 0;
  }
  
  .footer-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 30px;
  }
  
  .slogan {
    flex: 1 1 100%;
    max-width: 300px;
    margin-bottom: 30px;
  }
  
  .slogan-text {
    font-size: 1.8rem;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .about-section {
    flex: 1 1 100%;
    max-width: 400px;
    margin-bottom: 30px;
  }
  
  .about-title {
    font-size: 1.6rem;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .underline {
    border-top: 2px solid #fff;
    width: 50%;
    margin: 0 auto 15px auto;
  }
  
  .about-text {
    font-size: 1.4rem;
    line-height: 1.6;
  }
  
  .social-media {
    flex: 1 1 100%;
    max-width: 200px;
  }
  
  .social-title {
    font-size: 1.6rem;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .social-icons {
    display: flex;
    justify-content: space-between;
  }
  
  .social-link img {
    width: 30px;
    height: auto;
  }
  </style>