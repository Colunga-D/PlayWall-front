<template>
  <div id="app">
    <HeaderComp :mostrarHeader="mostrarHeader" />
    <router-view />
    <FooterComp />
  </div>
</template>

<script setup>
import HeaderComp from './components/HeaderComp.vue';
import FooterComp from './components/FooterComp.vue';
import { useRoute } from 'vue-router';

const route = useRoute();
const mostrarHeader = route.name !== 'login' && route.name !== 'register'; // Ocultar el header en las vistas de login y registro
</script>

<style scoped>
/* Estilos específicos de la aplicación */
</style>