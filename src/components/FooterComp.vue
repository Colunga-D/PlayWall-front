<template>
  <footer class="sports-footer">
    <div class="footer-content">
      <div class="about-section">
        <h4 class="about-title">Sobre PlayWall</h4>
        <hr class="underline">
        <p class="about-text">
          Somos una entidad enfocada en que las personas puedan encontrar gente con la que jugar y poder hacer deporte juntos. Si nunca has podido realizar esa actividad que tanto querías, ahora es tu momento, ¡diviértete!
        </p>
      </div>
      <div class="slogan">
        <h3 class="slogan-text">Play With All</h3>
        <p class="slogan-description">Rompe el muro y juega con nuevas personas</p>
      </div>
      <div class="social-media">
        <h4 class="social-title">Redes Sociales</h4>
        <div class="social-icons">
          <a href="https://www.facebook.com/login/?next=https%3A%2F%2Fwww.facebook.com%2F%3Flocale%3Des_ES" class="social-link">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-facebook" width="33" height="33" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
  <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
  <path d="M7 10v4h3v7h4v-7h3l1 -4h-4v-2a1 1 0 0 1 1 -1h3v-4h-3a5 5 0 0 0 -5 5v2h-3" />
</svg>
          </a>
          <a href="https://www.instagram.com/" class="social-link">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-instagram" width="33" height="33" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
  <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
  <path d="M4 4m0 4a4 4 0 0 1 4 -4h8a4 4 0 0 1 4 4v8a4 4 0 0 1 -4 4h-8a4 4 0 0 1 -4 -4z" />
  <path d="M12 12m-3 0a3 3 0 1 0 6 0a3 3 0 1 0 -6 0" />
  <path d="M16.5 7.5l0 .01" />
</svg>
          </a>
          <a href="https://www.google.com/?hl=es" class="social-link">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-google" width="33" height="33" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
  <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
  <path d="M20.945 11a9 9 0 1 1 -3.284 -5.997l-2.655 2.392a5.5 5.5 0 1 0 2.119 6.605h-4.125v-3h7.945z" />
</svg>
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
  justify-content: space-between;
  align-items: flex-start;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 30px;
}

.about-section {
  flex: 1 1 auto;
  max-width: 300px;
  text-align: left;
  margin-right: 150px;
}

.about-title {
  font-size: 1.6rem;
  font-weight: bold;
  margin-bottom: 5px;
}

.underline {
  border-top: 2px solid #fff;
  width: 100%;
  margin: 0;
}

.about-text {
  font-size: 1.4rem;
  line-height: 1.6;
}

.slogan {
  flex: 1 1 auto;
  text-align: center;
  max-width: 400px;
}

.slogan-text {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.slogan-description {
  font-size: 1.4rem;
}

.social-media {
  flex: 1 1 auto;
  text-align: right;
}

.social-title {
  font-size: 1.6rem;
  font-weight: bold;
  margin-bottom: 5px;
}

.social-icons {
  display: flex;
  justify-content: flex-end;
}

.social-link img {
  width: 30px;
  height: auto;
  margin-left: 10px;
}
</style>