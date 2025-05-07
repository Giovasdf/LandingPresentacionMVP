<template>
  <div class="bg-gray-900 py-12 sm:py-16">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center mb-12">
        <h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">Tecnologías Utilizadas</h2>
        <p class="mt-4 text-lg leading-8 text-gray-300">
          Stack tecnológico que potencia MediBot
        </p>
      </div>

      <!-- Marquee container -->
      <div class="relative overflow-hidden">
        <!-- Primer marquee (derecha a izquierda) -->
        <div class="flex items-center marquee">
          <div v-for="(tech, index) in technologies" :key="'first-' + index" class="mx-8 flex-shrink-0">
            <div class="flex flex-col items-center">
              <img :src="tech.logo" :alt="tech.name"
                class="h-16 w-16 object-contain grayscale hover:grayscale-0 transition-all duration-300">
              <span class="mt-2 text-sm font-medium text-gray-300">{{ tech.name }}</span>
            </div>
          </div>
        </div>

        <!-- Segundo marquee (izquierda a derecha, para efecto continuo) -->
        <div class="flex items-center marquee marquee-reverse">
          <div v-for="(tech, index) in technologies" :key="'second-' + index" class="mx-8 flex-shrink-0">
            <div class="flex flex-col items-center">
              <img :src="tech.logo" :alt="tech.name"
                class="h-16 w-16 object-contain grayscale hover:grayscale-0 transition-all duration-300">
              <span class="mt-2 text-sm font-medium text-gray-300">{{ tech.name }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const technologies = ref([
  { name: 'Vue.js', logo: 'https://upload.wikimedia.org/wikipedia/commons/9/95/Vue.js_Logo_2.svg' },
  { name: 'Vite', logo: 'https://vitejs.dev/logo.svg' },
  { name: 'Node.js', logo: 'https://nodejs.org/static/images/logo.svg' },
  { name: 'Express', logo: 'https://upload.wikimedia.org/wikipedia/commons/6/64/Expressjs.png' },
  { name: 'PocketBase', logo: 'https://files.raycast.com/3ypz5c7hya8x5lltm3z7pn7ik5zh' },
  { name: 'Twilio', logo: 'https://www.vectorlogo.zone/logos/twilio/twilio-icon.svg' },
  { name: 'Mistral 7B', logo: 'https://avatars.githubusercontent.com/u/148980147?s=200&v=4' }, // Mistral AI GitHub avatar
  { name: 'Railway', logo: 'https://railway.app/brand/logo-light.png' },
  { name: 'Heroku', logo: 'https://www.vectorlogo.zone/logos/heroku/heroku-icon.svg' },
  { name: 'Cypress', logo: 'https://assets.streamlinehq.com/image/private/w_300,h_300,ar_1/f_auto/v1/icons/3/cypress-icon-moigrz5nimpd7rsob0bisu.png/cypress-icon-pg9bdlubveoefqouilbg.png?_a=DATAdtAAZAA0' },
  { name: 'Vitest', logo: 'https://vitest.dev/logo.svg' },
]);

</script>

<style scoped>
.marquee {
  display: flex;
  animation: scroll 30s linear infinite;
  width: calc(200%);
}

.marquee-reverse {
  animation: scrollReverse 30s linear infinite;
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }

  100% {
    transform: translateX(-50%);
  }
}

@keyframes scrollReverse {
  0% {
    transform: translateX(-50%);
  }

  100% {
    transform: translateX(0);
  }
}

/* Efecto hover para pausar la animación */
.marquee:hover,
.marquee-reverse:hover {
  animation-play-state: paused;
}

/* Ajustes para móviles */
@media (max-width: 640px) {

  .marquee,
  .marquee-reverse {
    animation-duration: 20s;
  }

  img {
    height: 12vw;
    width: 12vw;
  }
}
</style>
