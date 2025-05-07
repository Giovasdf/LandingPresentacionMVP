<template>
  <div class="bg-gray-900 min-h-screen py-12">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div
        class="relative isolate overflow-hidden bg-gray-800 px-6 pt-16 shadow-2xl sm:rounded-3xl sm:px-16 md:pt-24 lg:flex lg:gap-x-20 lg:px-24 lg:pt-12">
        <svg viewBox="0 0 1024 1024"
          class="absolute top-1/2 left-1/2 -z-10 h-[64rem] w-[64rem] -translate-y-1/2 [mask-image:radial-gradient(closest-side,white,transparent)] sm:left-full sm:-ml-80 lg:left-1/2 lg:ml-0 lg:-translate-x-1/2 lg:translate-y-0"
          aria-hidden="true">
          <circle cx="512" cy="512" r="512" fill="url(#759c1415-0410-454c-8f7c-9a820de03641)" fill-opacity="0.2" />
          <defs>
            <radialGradient id="759c1415-0410-454c-8f7c-9a820de03641">
              <stop stop-color="#4F46E5" />
              <stop offset="1" stop-color="#9333EA" />
            </radialGradient>
          </defs>
        </svg>

        <div class="mx-auto max-w-md text-center lg:mx-0 lg:flex-auto lg:py-16 lg:text-left">
          <h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">
            Instrucciones para Conectarse a MediBot
          </h2>
          <p class="mt-4 text-lg leading-7 text-gray-300">
            Sigue estos sencillos pasos para empezar a interactuar con el sistema de pedidos de MediBot vía WhatsApp:
          </p>

          <div class="mt-8 text-lg text-gray-300">
            <ol class="space-y-4">
              <li class="flex items-start">
                <span
                  class="mr-3 flex h-6 w-6 flex-shrink-0 items-center justify-center rounded-full bg-indigo-500 text-white">1</span>
                <span>Abre WhatsApp en tu dispositivo móvil o en la versión web.</span>
              </li>
              <li class="flex items-start">
                <span
                  class="mr-3 flex h-6 w-6 flex-shrink-0 items-center justify-center rounded-full bg-indigo-500 text-white">2</span>
                <span>Envía un mensaje al número <strong class="text-white">+1 415 523 8886</strong> con el código: <br>
                  <code
                    class="mt-1 inline-block rounded bg-gray-700 px-2 py-1 font-mono text-white">join pig-check</code>
                </span>
              </li>
              <li class="flex items-start">
                <span
                  class="mr-3 flex h-6 w-6 flex-shrink-0 items-center justify-center rounded-full bg-indigo-500 text-white">3</span>
                <span>Recibirás un mensaje de bienvenida con las opciones para realizar pedidos de productos
                  farmacéuticos.</span>
              </li>
            </ol>
          </div>

          <div class="mt-10 flex items-center justify-center gap-x-6 lg:justify-start">
            <a href="https://wa.me/14155238886?text=join%20pig-check" target="_blank"
              class="rounded-md bg-indigo-600 px-4 py-3 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
              Conectar con WhatsApp
            </a>
            <a href="#learn-more" class="text-sm font-semibold leading-6 text-gray-300 hover:text-white">
              Más información <span aria-hidden="true">→</span>
            </a>
          </div>
        </div>

        <div class="relative mt-16 lg:mt-0 lg:flex lg:items-center">
          <div class="mx-auto max-w-sm rounded-lg bg-white p-4 shadow-lg">
            <h3 class="text-center text-lg font-semibold text-gray-900">Escanea el código QR</h3>
            <p class="mt-1 text-center text-sm text-gray-600">Usa la cámara de WhatsApp para conectarte directamente</p>
            <img :src="qrCodeSrc" alt="QR Code para WhatsApp" class="mx-auto mt-4 h-48 w-48" />
            <p class="mt-3 text-center text-xs text-gray-500">o haz clic en el botón "Conectar con WhatsApp"</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
// Generando el src del QR de forma dinámica usando la imagen SVG proporcionada
const qrCodeSrc = "data:image/svg+xml;utf8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%2033%2033%22%20shape-rendering%3D%22crispEdges%22%3E%3Cpath%20fill%3D%22%23ffffff%22%20d%3D%22M0%200h33v33H0z%22%2F%3E%3Cpath%20stroke%3D%22%23000000%22%20d%3D%22M0%200.5h7m2%200h1m1%200h9m3%200h2m1%200h7M0%201.5h1m5%200h1m2%200h1m2%200h3m2%200h1m4%200h1m3%200h1m5%200h1M0%202.5h1m1%200h3m1%200h1m1%200h6m1%200h4m4%200h1m2%200h1m1%200h3m1%200h1M0%203.5h1m1%200h3m1%200h1m1%200h4m2%200h3m2%200h6m1%200h1m1%200h3m1%200h1M0%204.5h1m1%200h3m1%200h1m1%200h1m1%200h1m1%200h2m1%200h1m1%200h2m5%200h1m1%200h1m1%200h3m1%200h1M0%205.5h1m5%200h1m1%200h2m3%200h4m3%200h1m3%200h1m1%200h1m5%200h1M0%206.5h7m1%200h1m1%200h1m1%200h1m1%200h1m1%200h1m1%200h1m1%200h1m1%200h1m1%200h7M8%207.5h2m1%200h3m1%200h1m2%200h1m2%200h3M0%208.5h1m1%200h5m2%200h4m1%200h4m3%200h1m2%200h1m1%200h5M1%209.5h2m1%200h1m2%200h1m2%200h1m1%200h1m1%200h3m3%200h7m2%200h2m1%200h1M0%2010.5h1m5%200h5m7%200h2m1%200h1m4%200h1m1%200h1m1%200h2M3%2011.5h3m1%200h5m2%200h1m4%200h1m1%200h2m3%200h1m1%200h3m1%200h1M3%2012.5h1m2%200h3m1%200h1m7%200h2m1%200h1m3%200h2m2%200h1m2%200h1M0%2013.5h2m10%200h6m2%200h3m6%200h4M2%2014.5h1m3%200h2m1%200h2m1%200h2m3%200h1m1%200h1m1%200h1m1%200h3m1%200h2m1%200h2M2%2015.5h1m1%200h2m2%200h1m2%200h3m2%200h6m1%200h1m1%200h2m1%200h3M0%2016.5h2m1%200h1m2%200h2m1%200h1m1%200h2m3%200h2m1%200h1m4%200h2m1%200h2m3%200h1M1%2017.5h1m1%200h1m3%200h1m5%200h1m2%200h3m1%200h1m2%200h1m2%200h2m1%200h2M2%2018.5h2m1%200h2m5%200h4m1%200h1m4%200h1m2%200h1m2%200h1m1%200h2M2%2019.5h1m2%200h1m1%200h3m5%200h1m1%200h2m7%200h1m1%200h3M0%2020.5h1m1%200h5m1%200h2m3%200h1m2%200h1m2%200h9m1%200h1m1%200h2M0%2021.5h2m5%200h1m2%200h1m1%200h1m2%200h1m1%200h2m6%200h1m2%200h1m1%200h1m1%200h1M0%2022.5h1m2%200h1m2%200h2m1%200h1m3%200h1m1%200h2m1%200h1m1%200h5m2%200h2m1%200h2M0%2023.5h1m2%200h2m3%200h1m1%200h2m1%200h1m1%200h1m1%200h2m4%200h3m1%200h1m1%200h1m2%200h1M0%2024.5h1m1%200h1m1%200h3m1%200h1m3%200h1m1%200h2m4%200h2m1%200h6m2%200h2M8%2025.5h3m1%200h1m3%200h1m1%200h1m2%200h1m2%200h1m3%200h1m1%200h2M0%2026.5h7m11%200h1m2%200h1m1%200h2m1%200h1m1%200h1m1%200h3M0%2027.5h1m5%200h1m1%200h2m5%200h1m3%200h1m1%200h4m3%200h1m1%200h1m1%200h1M0%2028.5h1m1%200h3m1%200h1m1%200h1m3%200h2m1%200h1m2%200h2m1%200h1m2%200h6M0%2029.5h1m1%200h3m1%200h1m1%200h2m3%200h5m2%200h1m1%200h1m4%200h2m1%200h1M0%2030.5h1m1%200h3m1%200h1m1%200h1m1%200h1m1%200h3m2%200h3m1%200h3m2%200h2m2%200h1M0%2031.5h1m5%200h1m2%200h1m2%200h3m1%200h5m1%200h1m1%200h1m2%200h3M0%2032.5h7m1%200h1m5%200h1m1%200h2m1%200h1m1%200h1m1%200h1m3%200h5%22%2F%3E%3C%2Fsvg%3E";
</script>
