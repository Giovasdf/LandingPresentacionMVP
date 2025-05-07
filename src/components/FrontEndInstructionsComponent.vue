<template>
  <div class="bg-gray-900 py-16 sm:py-24">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">Acceso al Panel de Administración</h2>
        <p class="mt-4 text-lg leading-8 text-gray-300">
          Credenciales para explorar el sistema de gestión de pedidos MediBot
        </p>
      </div>

      <div class="mt-16 flex flex-col lg:flex-row gap-12">
        <!-- Tarjeta de credenciales -->
        <div class="lg:w-1/2">
          <div class="rounded-xl overflow-hidden shadow-2xl bg-gray-800 p-8">
            <h3 class="text-2xl font-semibold text-white mb-6">Conéctate al login</h3>

            <div class="space-y-6">
              <div>
                <label class="block text-sm font-medium text-gray-400 mb-1">URL del sistema</label>
                <div class="flex rounded-md shadow-sm">
                  <input type="text" readonly value="https://mvpproyectotitulo-production.up.railway.app/login"
                    class="flex-1 min-w-0 block w-full px-3 py-2 rounded-l-md bg-gray-700 border border-gray-600 text-white text-sm">
                  <a href="https://mvpproyectotitulo-production.up.railway.app/login" target="_blank"
                    class="inline-flex items-center px-4 py-2 rounded-r-md bg-indigo-600 text-sm font-medium text-white hover:bg-indigo-500 focus:outline-none">
                    Ir
                  </a>
                </div>
              </div>

              <!-- Credenciales Admin -->
              <div class="border border-gray-700 rounded-lg p-4">
                <h4 class="text-lg font-medium text-white mb-3 flex items-center">
                  <svg class="h-5 w-5 text-yellow-400 mr-2" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd"
                      d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                      clip-rule="evenodd" />
                  </svg>
                  Rol Administrador
                </h4>
                <div class="space-y-3">
                  <div>
                    <label class="block text-sm font-medium text-gray-400 mb-1">Usuario</label>
                    <div class="relative">
                      <input type="text" readonly value="gmolina.dev@gmail.com"
                        class="w-full px-3 py-2 bg-gray-700 border border-gray-600 rounded-md text-white text-sm">
                      <button @click="copyToClipboard('gmolina.dev@gmail.com')"
                        class="absolute inset-y-0 right-0 pr-3 flex items-center" title="Copiar usuario">
                        <svg class="h-5 w-5 text-gray-400 hover:text-white" fill="none" viewBox="0 0 24 24"
                          stroke="currentColor">
                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
                        </svg>
                      </button>
                    </div>
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-400 mb-1">Contraseña</label>
                    <div class="relative">
                      <input :type="showAdminPass ? 'text' : 'password'" readonly value="giovanni123."
                        class="w-full px-3 py-2 bg-gray-700 border border-gray-600 rounded-md text-white text-sm">
                      <div class="absolute inset-y-0 right-0 pr-3 flex items-center space-x-2">
                        <button @click="toggleShow('admin')" title="Mostrar contraseña">
                          <svg class="h-5 w-5 text-gray-400 hover:text-white" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                          </svg>
                        </button>
                        <button @click="copyToClipboard('giovanni123.')" title="Copiar contraseña">
                          <svg class="h-5 w-5 text-gray-400 hover:text-white" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
                          </svg>
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Credenciales Operador -->
              <div class="border border-gray-700 rounded-lg p-4">
                <h4 class="text-lg font-medium text-white mb-3 flex items-center">
                  <svg class="h-5 w-5 text-blue-400 mr-2" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd"
                      d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.084A5 5 0 0010 11z"
                      clip-rule="evenodd" />
                  </svg>
                  Rol Operador
                </h4>
                <div class="space-y-3">
                  <div>
                    <label class="block text-sm font-medium text-gray-400 mb-1">Usuario</label>
                    <div class="relative">
                      <input type="text" readonly value="thalitacmartins@gmail.com"
                        class="w-full px-3 py-2 bg-gray-700 border border-gray-600 rounded-md text-white text-sm">
                      <button @click="copyToClipboard('thalitacmartins@gmail.com')"
                        class="absolute inset-y-0 right-0 pr-3 flex items-center" title="Copiar usuario">
                        <svg class="h-5 w-5 text-gray-400 hover:text-white" fill="none" viewBox="0 0 24 24"
                          stroke="currentColor">
                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
                        </svg>
                      </button>
                    </div>
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-400 mb-1">Contraseña</label>
                    <div class="relative">
                      <input :type="showOperatorPass ? 'text' : 'password'" readonly value="thalita123."
                        class="w-full px-3 py-2 bg-gray-700 border border-gray-600 rounded-md text-white text-sm">
                      <div class="absolute inset-y-0 right-0 pr-3 flex items-center space-x-2">
                        <button @click="toggleShow('operator')" title="Mostrar contraseña">
                          <svg class="h-5 w-5 text-gray-400 hover:text-white" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                          </svg>
                        </button>
                        <button @click="copyToClipboard('thalita123.')" title="Copiar contraseña">
                          <svg class="h-5 w-5 text-gray-400 hover:text-white" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
                          </svg>
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Imagen del login -->
        <div class="lg:w-1/2 flex items-center">
          <div class="rounded-xl overflow-hidden shadow-2xl bg-gray-800 w-full">
            <div class="p-4 bg-gray-700">
              <div class="flex space-x-2">
                <div class="w-3 h-3 rounded-full bg-red-500"></div>
                <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
                <div class="w-3 h-3 rounded-full bg-green-500"></div>
              </div>
            </div>
            <div class="bg-black flex items-center justify-center">
              <img :src="LoginImage" alt="Pantalla de login del sistema MediBot" class="w-full h-auto object-contain" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import LoginImage from '@/assets/image.png';

const showAdminPass = ref(false);
const showOperatorPass = ref(false);
const showToast = ref(false);
const toastMessage = ref('');

const toggleShow = (role) => {
  if (role === 'admin') {
    showAdminPass.value = !showAdminPass.value;
  } else {
    showOperatorPass.value = !showOperatorPass.value;
  }
};

const copyToClipboard = (text) => {
  navigator.clipboard.writeText(text);
  toastMessage.value = `"${text}" copiado al portapapeles`;
  showToast.value = true;
  setTimeout(() => showToast.value = false, 3000);
};
</script>

<style scoped>
/* Estilos para la notificación toast */
.toast {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-color: #4F46E5;
  color: white;
  padding: 12px 24px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  z-index: 50;
  animation: fadeInOut 3s ease-in-out;
}

@keyframes fadeInOut {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }

  10% {
    opacity: 1;
    transform: translateY(0);
  }

  90% {
    opacity: 1;
    transform: translateY(0);
  }

  100% {
    opacity: 0;
    transform: translateY(20px);
  }
}
</style>
