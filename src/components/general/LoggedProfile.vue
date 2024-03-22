<script setup>
import { useAuthStore } from './../../../stores/AuthStore';

const authStore = useAuthStore();
</script>

<template>
 <div class="logged-profile">
    <img src="/icons/icon-user.svg" alt="user icon" class="user-icon">
    <p> {{ authStore.username }} </p>
    <img src="/icons/icon-log-out.svg" alt="log out icon" class="logout-icon" @click="authStore.logout">
 </div>
</template>

<style scoped lang="scss">
.logged-profile {
 display: flex;
 align-items: center;
 gap: 1rem;
 padding: 0.5rem;
 border-radius: 10px;
 background-color: rgba(255, 255, 255, 0.8);
 box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.user-icon, .logout-icon {
 height: 2rem;
 width: 2rem;
}

p {
 font-family: "Poppins", sans-serif;
 font-weight: 300;
 color: $primary-color;
 font-size: 1.4rem;
}
</style>