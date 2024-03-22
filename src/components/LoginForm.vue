<template>
    <div class="login-container">
       <div class="login-form">
         <h2 class="login-title">Iniciar Sesión</h2>
         <form @submit.prevent="handleSubmit">
           <div class="form-group">
             <label for="username">Nombre de Usuario</label>
             <input type="text" id="username" v-model="username" required>
           </div>
           <div class="form-group">
             <label for="password">Contraseña</label>
             <input type="password" id="password" v-model="password" required>
           </div>
           <button type="submit" :disabled="isLoading">
             <span v-if="isLoading" class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
             Iniciar Sesión
           </button>
         </form>
         <p v-if="error" class="error-message">{{ error }}</p>
       </div>
    </div>
   </template>
   
   <script>
//    import axios from 'axios';
   import { useRouter } from 'vue-router';
   
   export default {
    data() {
       return {
         username: '',
         password: '',
         isLoading: false,
         error: null
       };
    },
    methods: {
       async handleSubmit() {
         this.isLoading = true;
         this.error = null;
         const router = useRouter();
         try {
           const response = await axios.post('URL_DE_TU_API', {
             username: this.username,
             password: this.password
           });
           console.log('Inicio de sesión exitoso:', response.data);
           router.push({ name: 'HomeView' });
         } catch (error) {
           this.error = 'Nombre de usuario o contraseña incorrectos';
         } finally {
           this.isLoading = false;
         }
       }
    }
   };
   </script>
   
   <style scoped>
   .login-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    position: relative; /* Posicionamiento relativo para la imagen de fondo */
   }
   
   .login-container::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: url('/public/images/photo_1_boys_soccerkick.jpg') no-repeat center center fixed;
    background-size: cover;
    filter: blur(2px); /* Aplica el efecto de difuminación a la imagen de fondo */
    z-index: -1; /* Asegura que la imagen esté detrás del contenido */
   }
   
   .login-form {
    width: 100%;
    max-width: 400px;
    padding: 40px;
    background-color: rgba(255, 255, 255, 0.8);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
   }
   
   .login-title {
    font-size: 2.5rem;
    color: #333;
    text-align: center;
    margin-bottom: 20px;
   }
   
   .form-group {
    margin-bottom: 20px;
   }
   
   .form-group label {
    display: block;
    margin-bottom: 5px;
   }
   
   .form-group input {
    width: 100%;
    padding: 15px;
    border: 1px solid #ddd;
    border-radius: 4px;
   }
   
   button {
    width: 100%;
    padding: 15px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1.2rem;
   }
   
   button:hover {
    background-color: #0056b3;
   }
   
   button:disabled {
    background-color: #ccc;
    cursor: not-allowed;
   }
   
   .spinner-border {
    margin-right: 5px;
   }
   
   .error-message {
    color: red;
   }
   
   @media (max-width: 768px) {
    .login-form {
       max-width: 90%;
       padding: 20px;
    }
   }
   </style>