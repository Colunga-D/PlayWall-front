<template>
  <header v-if="mostrarHeader" class="header">

    <div class="header-content">
      <div class="left-section">
        <div class="logo-container">
          <img src="/public/images/logo.png" alt="Logo de PlayWall" class="logo">
          <h1 class="company-name">PlayWall</h1>
        </div>
      </div>
      <nav class="main-nav">
        <div class="nav-item" @mouseover="showDropdown = true" @mouseleave="showDropdown = false">
          <a href="#" class="nav-link">Deportes</a>
          <div v-if="showDropdown" class="dropdown-menu">
            <router-link to="/soccer" class="dropdown-item">Fútbol</router-link>
            <router-link to="/basketball" class="dropdown-item">Baloncesto</router-link>
            <router-link to="/tennis" class="dropdown-item">Tenis</router-link>
          </div>
        </div>
        <router-link to="/news" class="nav-link">Noticias</router-link>
        <router-link to="/contact" class="nav-link">Contacto</router-link>
      </nav>
      <div class="right-section">
        <div class="actions-container">
          <router-link to="/login" class="login-button">Iniciar sesión</router-link>
          <router-link to="/register" class="register-button">Registrarse</router-link>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
 let mostrarHeader = true;
import { ref } from 'vue';

const showDropdown = ref(false);
</script>

<style scoped lang="scss">
.header {
  background-color: #1a1a1a;
  color: #fff;
  padding: 30px 0;
  position: fixed;
  width: 100%;
  z-index: 1000;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 30px;
}

.left-section,
.right-section {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.logo-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-bottom: 20px;
}

.logo {
  height: 70px;
}

.company-name {
  font-size: 2.5rem;
  font-weight: bold;
}

.main-nav {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}

.nav-link {
  color: #fff;
  text-decoration: none;
  margin-right: 20px;
  transition: color 0.3s ease;
  font-size: 1.8rem;
  font-weight: bold;
}

.nav-link:hover {
  color: #ddd;
}

.actions-container {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.login-button,
.register-button {
  background-color: #fff;
  color: #000;
  border: none;
  padding: 15px 40px;
  margin-left: 30px;
  cursor: pointer;
  transition: background-color 0.3s ease;
  border-radius: 50px;
  font-size: 1.4rem;
}

.login-button:hover,
.register-button:hover {
  background-color: #ddd;
}

.dropdown-menu {
  position: absolute;
  background-color: #5c5c5c;
  padding: 15px;
  border-radius: 5px;
  width: 250px;
}

.dropdown-item {
  display: block;
  color: #fff;
  padding: 10px 0;
}

.dropdown-item:hover {
  color: #ddd;
}

@media (max-width: 767px) {
  .header-content {
    flex-direction: column;
    align-items: flex-start;
  }

  .left-section,
  .right-section {
    align-items: center;
  }

  .nav-link {
    margin-right: 10px;
  }

  .actions-container {
    justify-content: center;
  }
}
</style>