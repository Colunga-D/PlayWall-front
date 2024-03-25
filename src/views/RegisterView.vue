<template>
    <div class="register-background">
      <div class="register-container">
        <h1 class="register-title">¡Únete a nosotros!</h1>
        <form @submit.prevent="submitForm">
          <div class="form-group">
            <label for="username">Nombre de usuario</label>
            <input type="text" id="username" v-model="formData.username" required>
          </div>
          <div class="form-group">
            <label for="email">Correo electrónico</label>
            <input type="email" id="email" v-model="formData.email" required>
          </div>
          <div class="form-group">
            <label for="password">Contraseña</label>
            <input type="password" id="password" v-model="formData.password" required>
          </div>
          <div class="form-group">
            <label for="confirmPassword">Confirmar contraseña</label>
            <input type="password" id="confirmPassword" v-model="confirmPassword" required>
          </div>
          <div class="form-group">
            <button type="submit">Registrarse</button>
          </div>
        </form>
        <p v-if="successMessage" class="success-message">{{ successMessage }}</p>
        <p v-if="errorMessage" class="error-message">{{ errorMessage }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import { useRouter } from 'vue-router';
  
  const router = useRouter();
  
  const formData = ref({
    username: '',
    email: '',
    password: ''
  });
  
  const confirmPassword = ref('');
  
  const successMessage = ref('');
  const errorMessage = ref('');
  
  const submitForm = () => {
    if (formData.value.password !== confirmPassword.value) {
      errorMessage.value = 'Las contraseñas no coinciden.';
      return;
    }
  
    setTimeout(() => {
      successMessage.value = '¡Registro exitoso!';
      
      router.push({ name: 'home' });
      
      formData.value.username = '';
      formData.value.email = '';
      formData.value.password = '';
      confirmPassword.value = '';
    }, 1000);
  };
  </script>
  <style scoped>
  .register-background {
    background-image: url('/public/images/Protocolo\ deportistas.jpg');
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .register-container {
    background-color: rgba(255, 255, 255, 0.8); /* Fondo con opacidad */
    max-width: 400px;
    width: 90%;
    padding: 40px;
    border-radius: 8px;
    text-align: center;
  }
  
  .register-title {
    font-size: 2.5rem;
    color: #333; /* Color más oscuro */
    margin-bottom: 20px;
  }
  
  .form-group {
    margin-bottom: 20px;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
  }
  
  input[type="text"],
  input[type="email"],
  input[type="password"] {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  button {
    background-color: #007bff;
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  
  .success-message {
    color: #28a745;
  }
  
  .error-message {
    color: #dc3545;
  }
  
  @media (max-width: 768px) {
    .register-container {
      width: 100%;
    }
  }
  </style>