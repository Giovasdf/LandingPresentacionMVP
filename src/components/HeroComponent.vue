<template>
  <div class="bg-gray-900 text-white">
    <!-- Fondo con efectos -->
    <div class="relative isolate px-6 pt-20 lg:px-8">
      <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
        aria-hidden="true">
        <div
          class="relative left-[calc(50%-11rem)] aspect-1155/678 w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]"
          style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)">
        </div>
      </div>

      <!-- Contenido principal -->
      <div class="mx-auto max-w-4xl py-20 sm:py-32 lg:py-40 text-center">
        <!-- Título principal -->
        <h1 class="text-4xl mb-20 font-semibold sm:text-5xl lg:text-6xl text-white leading-tight">
          MediBot: Gestión Automática de Pedidos en Farmacias vía WhatsApp e Inteligencia Artificial
        </h1>

        <!-- Descripción -->
        <p class="mt-6 text-lg leading-8 text-gray-300 text-justify">
          <strong>Estudiante:</strong> Giovanni Molina<br>
          <strong>Docente:</strong> Mauricio Hidalgo Barrientos<br>
          <strong>Institución:</strong> IPLACEX<br>
          <strong>Fecha:</strong>20-Mayo-2025
        </p>


      </div>

      <!-- Fondo adicional con blur -->
      <div
        class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]"
        aria-hidden="true">
        <div
          class="relative left-[calc(50%+3rem)] aspect-1155/678 w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]"
          style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)">
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
// Aquí puedes agregar funciones si es necesario, actualmente no es necesario.
</script>

<style scoped>
/* Agregamos algunos estilos adicionales para mejorar la animación de los botones y efectos */
.text-justify {
  text-align: justify;
}

/* Mejora en los bordes de los botones y las transiciones */
a:hover {
  transition: all 0.3s ease-in-out;
  transform: scale(1.05);
}
</style>
