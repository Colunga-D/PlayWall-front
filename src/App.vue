<script setup>
import { RouterLink, RouterView } from 'vue-router'
import FooterCompVue from './components/FooterComp.vue'
import HeaderCompVue from './components/HeaderComp.vue'


</script>

<template>


<HeaderCompVue/>
  <RouterView />
<FooterCompVue/>

</template>

<style scoped>
</style>