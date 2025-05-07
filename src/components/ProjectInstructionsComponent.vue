<template>
  <div class="bg-gray-900 py-16 sm:py-24">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">Cómo Levantar el Proyecto</h2>
        <p class="mt-4 text-lg leading-8 text-gray-300">
          Instrucciones para configurar el entorno de desarrollo
        </p>
      </div>

      <div class="mt-16 grid grid-cols-1 gap-12 lg:grid-cols-3">
        <!-- Frontend (Vue) -->
        <div class="rounded-xl overflow-hidden shadow-2xl bg-gray-800">
          <div class="p-6 bg-indigo-600">
            <h3 class="text-xl font-semibold text-white">Frontend Vue.js</h3>
          </div>
          <div class="p-6">
            <div class="space-y-6">
              <div>
                <h4 class="text-lg font-medium text-white mb-3">Repositorio</h4>
                <div class="bg-gray-700 p-3 rounded-md overflow-x-auto">
                  <code class="text-indigo-300 text-sm break-all">
                    https://github.com/Giovasdf/MVPProyectoTitulo.git
                  </code>
                  <button @click="copyToClipboard('https://github.com/Giovasdf/MVPProyectoTitulo.git')"
                    class="mt-2 flex items-center text-xs text-indigo-400 hover:text-indigo-300">
                    <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
                    </svg>
                    Copiar URL
                  </button>
                </div>
              </div>

              <div>
                <h4 class="text-lg font-medium text-white mb-3">Instalación</h4>
                <div class="space-y-3">
                  <div class="flex flex-col">
                    <span class="text-sm text-gray-400 mb-1">1. Clonar repositorio</span>
                    <div class="bg-gray-700 p-3 rounded-md overflow-x-auto">
                      <code class="text-white text-sm break-all">
                        git clone https://github.com/Giovasdf/MVPProyectoTitulo.git
                      </code>
                    </div>
                  </div>
                  <div class="flex flex-col">
                    <span class="text-sm text-gray-400 mb-1">2. Entrar al directorio</span>
                    <div class="bg-gray-700 p-3 rounded-md">
                      <code class="text-white text-sm">
                        cd MVPProyectoTitulo
                      </code>
                    </div>
                  </div>
                  <div class="flex flex-col">
                    <span class="text-sm text-gray-400 mb-1">3. Instalar dependencias</span>
                    <div class="bg-gray-700 p-3 rounded-md">
                      <code class="text-white text-sm">
                        npm install
                      </code>
                    </div>
                  </div>
                </div>
              </div>

              <div>
                <h4 class="text-lg font-medium text-white mb-3">Ejecución</h4>
                <div class="bg-gray-700 p-3 rounded-md">
                  <code class="text-white text-sm">
                    npm run dev
                  </code>
                </div>
                <p class="mt-2 text-sm text-gray-400">El frontend estará disponible en http://localhost:5173</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Backend (Node) -->
        <div class="rounded-xl overflow-hidden shadow-2xl bg-gray-800">
          <div class="p-6 bg-green-600">
            <h3 class="text-xl font-semibold text-white">Backend Node.js</h3>
          </div>
          <div class="p-6">
            <div class="space-y-6">
              <div>
                <h4 class="text-lg font-medium text-white mb-3">Repositorio</h4>
                <div class="bg-gray-700 p-3 rounded-md overflow-x-auto">
                  <code class="text-green-300 text-sm break-all">
                    https://github.com/Giovasdf/MVPBackend.git
                  </code>
                  <button @click="copyToClipboard('https://github.com/Giovasdf/MVPBackend.git')"
                    class="mt-2 flex items-center text-xs text-green-400 hover:text-green-300">
                    <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
                    </svg>
                    Copiar URL
                  </button>
                </div>
              </div>

              <div>
                <h4 class="text-lg font-medium text-white mb-3">Instalación</h4>
                <div class="space-y-3">
                  <div class="flex flex-col">
                    <span class="text-sm text-gray-400 mb-1">1. Clonar repositorio</span>
                    <div class="bg-gray-700 p-3 rounded-md overflow-x-auto">
                      <code class="text-white text-sm break-all">
                        git clone https://github.com/Giovasdf/MVPBackend.git
                      </code>
                    </div>
                  </div>
                  <div class="flex flex-col">
                    <span class="text-sm text-gray-400 mb-1">2. Entrar al directorio</span>
                    <div class="bg-gray-700 p-3 rounded-md">
                      <code class="text-white text-sm">
                        cd MVPBackend
                      </code>
                    </div>
                  </div>
                  <div class="flex flex-col">
                    <span class="text-sm text-gray-400 mb-1">3. Instalar dependencias</span>
                    <div class="bg-gray-700 p-3 rounded-md">
                      <code class="text-white text-sm">
                        npm install
                      </code>
                    </div>
                  </div>
                </div>
              </div>

              <div>
                <h4 class="text-lg font-medium text-white mb-3">Ejecución</h4>
                <div class="bg-gray-700 p-3 rounded-md">
                  <code class="text-white text-sm">
                    npm run start
                  </code>
                </div>
                <p class="mt-2 text-sm text-gray-400">El backend estará disponible en http://localhost:3000</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Base de datos (PocketBase) -->
        <div class="rounded-xl overflow-hidden shadow-2xl bg-gray-800">
          <div class="p-6 bg-purple-600">
            <h3 class="text-xl font-semibold text-white">Base de Datos PocketBase</h3>
          </div>
          <div class="p-6">
            <div class="space-y-6">
              <div>
                <h4 class="text-lg font-medium text-white mb-3">Repositorio</h4>
                <div class="bg-gray-700 p-3 rounded-md overflow-x-auto">
                  <code class="text-purple-300 text-sm break-all">
                    https://github.com/Giovasdf/DATABASE-MVP.git
                  </code>
                  <button @click="copyToClipboard('https://github.com/Giovasdf/DATABASE-MVP.git')"
                    class="mt-2 flex items-center text-xs text-purple-400 hover:text-purple-300">
                    <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
                    </svg>
                    Copiar URL
                  </button>
                </div>
              </div>

              <div>
                <h4 class="text-lg font-medium text-white mb-3">Instalación</h4>
                <div class="space-y-3">
                  <div class="flex flex-col">
                    <span class="text-sm text-gray-400 mb-1">1. Clonar repositorio</span>
                    <div class="bg-gray-700 p-3 rounded-md overflow-x-auto">
                      <code class="text-white text-sm break-all">
                        git clone https://github.com/Giovasdf/DATABASE-MVP.git
                      </code>
                    </div>
                  </div>
                  <div class="flex flex-col">
                    <span class="text-sm text-gray-400 mb-1">2. Entrar al directorio</span>
                    <div class="bg-gray-700 p-3 rounded-md">
                      <code class="text-white text-sm">
                        cd DATABASE-MVP
                      </code>
                    </div>
                  </div>
                </div>
              </div>

              <div>
                <h4 class="text-lg font-medium text-white mb-3">Ejecución</h4>
                <div class="bg-gray-700 p-3 rounded-md">
                  <code class="text-white text-sm">
                    ./pocketbase serve
                  </code>
                </div>
                <p class="mt-2 text-sm text-gray-400">PocketBase estará disponible en http://localhost:8090</p>
                <p class="mt-2 text-xs text-gray-500">* Asegúrate de tener permisos de ejecución en el archivo</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="mt-12 bg-gray-800 rounded-xl p-6 border border-gray-700">
        <h3 class="text-lg font-medium text-white mb-4">Notas Adicionales</h3>
        <ul class="space-y-3 text-gray-300">
          <li class="flex items-start">
            <svg class="h-5 w-5 text-yellow-400 mr-2 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-11a1 1 0 10-2 0v3.586L7.707 9.293a1 1 0 00-1.414 1.414l3 3a1 1 0 001.414 0l3-3a1 1 0 00-1.414-1.414L11 10.586V7z"
                clip-rule="evenodd" />
            </svg>
            <span>Asegúrate de tener Node.js (v16+) y npm instalados</span>
          </li>
          <li class="flex items-start">
            <svg class="h-5 w-5 text-yellow-400 mr-2 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-11a1 1 0 10-2 0v3.586L7.707 9.293a1 1 0 00-1.414 1.414l3 3a1 1 0 001.414 0l3-3a1 1 0 00-1.414-1.414L11 10.586V7z"
                clip-rule="evenodd" />
            </svg>
            <span>Configura las variables de entorno necesarias en cada proyecto</span>
          </li>
          <li class="flex items-start">
            <svg class="h-5 w-5 text-yellow-400 mr-2 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-11a1 1 0 10-2 0v3.586L7.707 9.293a1 1 0 00-1.414 1.414l3 3a1 1 0 001.414 0l3-3a1 1 0 00-1.414-1.414L11 10.586V7z"
                clip-rule="evenodd" />
            </svg>
            <span>Ejecuta los servicios en el orden: PocketBase → Backend → Frontend</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const copyToClipboard = (text: string) => {
  navigator.clipboard.writeText(text);
  alert(`"${text}" copied to clipboard`);
};

</script>
