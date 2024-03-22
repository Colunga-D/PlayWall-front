<template>
    <header>
      <div>
        <div>
          <img src="/images/logotype.png" alt="PrintGo logotype">
        </div>

        <div id="actions_container">
          <!-- Eliminamos los elementos de favoritos y carrito -->
          <HeaderButtons v-if="!authStore.isAuthenticated"/>
          <LoggedProfile v-if="authStore.isAuthenticated"/>
        </div>
        
      </div>

      <nav>
        <router-link to="/" exact-active-class="active">Inicio</router-link>
        <router-link to="/about" exact-active-class="active">Pádel</router-link>
        <router-link to="/about" exact-active-class="active">Fútbol</router-link>
        <router-link to="/about" exact-active-class="active">Baloncesto</router-link>
      </nav>
    </header>
</template>

<script setup>
import HeaderButtons from "./header/HeaderButtons.vue";
import { useAuthStore } from "./../../stores/AuthStore";
import LoggedProfile from "./header/LoggedProfile.vue";

const authStore = useAuthStore();
</script>

<style lang="scss" scoped>
header {
 position: fixed;
 width: 100%;
 z-index: 998;

 > div {
    background-color: $primary-background;
    height: 10rem;
    padding: 0 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    filter: drop-shadow(0 0 0.5rem black);
 }
}

#actions_container {
 display: flex;
 justify-content: flex-end;
 align-items: center;
 gap: 2rem;
}

nav {
 background-color: $primary-background;
 height: 6rem;
 padding-left: 7rem;
 display: flex;
 align-items: center;
 gap: 3rem;

 a {
    font-family: "Poppins", sans-serif;
    font-weight: 300;
    color: $inactive-primary-color;
    font-size: 1.7rem;
    transition: all 0.2s ease-in-out;
 }
 a:hover {
    color: $primary-color;
 }
}
.active {
 color: $primary-color;
}
</style>