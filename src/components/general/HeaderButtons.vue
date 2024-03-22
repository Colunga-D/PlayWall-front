<script setup>
import LoginForm from "./LoginForm.vue";
import RegisterForm from "./RegisterForm.vue";
import { ref } from 'vue';

let showRegisterForm = ref(false);
let showLoginForm = ref(false);

const openRegisterForm = () => {
 showRegisterForm.value = true;
 showLoginForm.value = false;
};

const openLoginForm = () => {
 showLoginForm.value = true;
 showRegisterForm.value = false;
};

const closeForm = () => {
 showRegisterForm.value = false;
 showLoginForm.value = false;
};
</script>

<template>
 <div class="header-buttons">
    <div>
      <button @click="openLoginForm()" class="login-button">
        Iniciar sesión
      </button>
  
      <button @click="openRegisterForm()" class="register-button">
        Registrarse
      </button>
    </div>

    <div class="form-container">
      <RegisterForm v-if="showRegisterForm" @close="closeForm"/>
      <LoginForm v-if="showLoginForm" @close="closeForm"/>
    </div>
 </div>
</template>

<style scoped lang="scss">
.header-buttons {
 display: flex;
 flex-direction: column;
 align-items: center;
 gap: 1rem;
}

.login-button, .register-button {
 border: 2px solid $primary-color;
 height: 5rem;
 text-align: center;
 border-radius: 5px;
 padding: 0 2rem;
 font-size: 2rem;
 color: $primary-color;
 font-family: "Poppins", sans-serif;
 transition: all 0.2s ease-in-out;
}

.login-button:hover {
 background-color: $primary-color;
 color: $light-font;
}

.register-button:hover {
 background-color: $primary-color;
 color: $light-font;
}

.form-container {
 position: relative;
}
</style>