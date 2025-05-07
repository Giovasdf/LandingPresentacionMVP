<template>
  <div class="bg-gray-900 py-16 sm:py-24">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">Cómo interactuar con MediBot</h2>
        <p class="mt-4 text-lg leading-8 text-gray-300">
          Sigue esta conversación de ejemplo para entender cómo realizar pedidos a través de WhatsApp
        </p>
      </div>

      <div class="mt-16 flex flex-col lg:flex-row gap-12">
        <!-- Contenedor para el GIF cuadrangular -->
        <div class="lg:w-1/2 flex justify-center">
          <div class="relative rounded-xl overflow-hidden shadow-2xl bg-gray-800 w-full max-w-lg">
            <!-- Barra superior estilo ventana -->
            <div class="p-4 bg-gray-700">
              <div class="flex space-x-2">
                <div class="w-3 h-3 rounded-full bg-red-500"></div>
                <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
                <div class="w-3 h-3 rounded-full bg-green-500"></div>
              </div>
            </div>

            <!-- GIF cuadrangular - ajustado para mantener proporción 1:1 -->
            <div class="aspect-square bg-black flex items-center justify-center">
              <img :src="VideoFinal" alt="Demo de conversación con MediBot" class="w-full h-full object-contain" />
            </div>
          </div>
        </div>
        <!-- Sección de explicación -->
        <div class="lg:w-1/2">
          <div class="flow-root">
            <div class="-mb-8">
              <!-- Cada paso de la conversación -->
              <div class="relative pb-8">
                <div class="relative flex items-start space-x-3">
                  <div class="relative">
                    <div class="flex h-6 w-6 items-center justify-center rounded-full bg-indigo-600">
                      <span class="text-xs font-semibold text-white">1</span>
                    </div>
                  </div>
                  <div class="min-w-0 flex-1">
                    <div>
                      <div class="text-sm">
                        <span class="font-medium text-gray-400">Usuario envía:</span>
                        <span class="ml-1 text-white">"Hola"</span>
                      </div>
                      <p class="mt-1 text-sm text-gray-300">El bot responde con los términos y condiciones que deben ser
                        aceptados para continuar.</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="relative pb-8">
                <div class="relative flex items-start space-x-3">
                  <div class="relative">
                    <div class="flex h-6 w-6 items-center justify-center rounded-full bg-indigo-600">
                      <span class="text-xs font-semibold text-white">2</span>
                    </div>
                  </div>
                  <div class="min-w-0 flex-1">
                    <div>
                      <div class="text-sm">
                        <span class="font-medium text-gray-400">Usuario responde:</span>
                        <span class="ml-1 text-white">"Sí"</span>
                      </div>
                      <p class="mt-1 text-sm text-gray-300">El bot muestra el menú principal con las opciones
                        disponibles.</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="relative pb-8">
                <div class="relative flex items-start space-x-3">
                  <div class="relative">
                    <div class="flex h-6 w-6 items-center justify-center rounded-full bg-indigo-600">
                      <span class="text-xs font-semibold text-white">3</span>
                    </div>
                  </div>
                  <div class="min-w-0 flex-1">
                    <div>
                      <div class="text-sm">
                        <span class="font-medium text-gray-400">Usuario selecciona:</span>
                        <span class="ml-1 text-white">"1" (Hacer un pedido)</span>
                      </div>
                      <p class="mt-1 text-sm text-gray-300">El bot solicita el nombre completo de quien retirará el
                        pedido.</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="relative pb-8">
                <div class="relative flex items-start space-x-3">
                  <div class="relative">
                    <div class="flex h-6 w-6 items-center justify-center rounded-full bg-indigo-600">
                      <span class="text-xs font-semibold text-white">4</span>
                    </div>
                  </div>
                  <div class="min-w-0 flex-1">
                    <div>
                      <div class="text-sm">
                        <span class="font-medium text-gray-400">Usuario envía:</span>
                        <span class="ml-1 text-white">Nombre completo</span>
                      </div>
                      <p class="mt-1 text-sm text-gray-300">El bot indica cómo agregar productos (uno por línea) y
                        finalizar con "listo".</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="relative pb-8">
                <div class="relative flex items-start space-x-3">
                  <div class="relative">
                    <div class="flex h-6 w-6 items-center justify-center rounded-full bg-indigo-600">
                      <span class="text-xs font-semibold text-white">5</span>
                    </div>
                  </div>
                  <div class="min-w-0 flex-1">
                    <div>
                      <div class="text-sm">
                        <span class="font-medium text-gray-400">Usuario envía:</span>
                        <span class="ml-1 text-white">Productos y "listo"</span>
                      </div>
                      <p class="mt-1 text-sm text-gray-300">El bot confirma cada producto y pregunta si desea agregar
                        más.</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="relative">
                <div class="relative flex items-start space-x-3">
                  <div class="relative">
                    <div class="flex h-6 w-6 items-center justify-center rounded-full bg-indigo-600">
                      <span class="text-xs font-semibold text-white">6</span>
                    </div>
                  </div>
                  <div class="min-w-0 flex-1">
                    <div>
                      <div class="text-sm">
                        <span class="font-medium text-gray-400">Resultado final:</span>
                      </div>
                      <p class="mt-1 text-sm text-gray-300">El bot genera un resumen estructurado del pedido usando IA
                        (Mistral 7B) y lo convierte a JSON para el sistema. La farmacia recibe el pedido en su panel de
                        administración Vue.js y lo prepara.</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="mt-12 border-t border-gray-700 pt-8">
            <h3 class="text-lg font-medium text-white">Tecnologías detrás de esta interacción</h3>
            <div class="mt-4 flex flex-wrap gap-3">
              <span
                class="inline-flex items-center rounded-full bg-gray-800 px-3 py-1 text-sm font-medium text-indigo-200">Twilio
                API</span>
              <span
                class="inline-flex items-center rounded-full bg-gray-800 px-3 py-1 text-sm font-medium text-indigo-200">Node.js/Express</span>
              <span
                class="inline-flex items-center rounded-full bg-gray-800 px-3 py-1 text-sm font-medium text-indigo-200">Mistral
                7B (OpenRouter)</span>
              <span
                class="inline-flex items-center rounded-full bg-gray-800 px-3 py-1 text-sm font-medium text-indigo-200">PocketBase</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import VideoFinal from '@/assets/VideoFinalPagina.gif';
</script>
