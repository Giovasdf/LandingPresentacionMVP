<template>
  <footer class="bg-gray-900 border-t border-gray-800 transition-colors duration-300">
    <div class="mx-auto max-w-7xl px-6 py-12 sm:py-16 lg:px-8">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <!-- Logo y descripción -->
        <div class="space-y-6">
          <div class="flex items-center">
            <IconMediBot />
            <span class="ml-2 text-2xl font-bold text-white">MediBot</span>
          </div>
          <p class="text-sm leading-6 text-gray-300">
            Sistema automatizado de pedidos farmacéuticos mediante WhatsApp.
          </p>
          <div class="flex space-x-4">
            <a href="https://github.com/Giovasdf/" target="_blank" class="text-gray-400 hover:text-white">
              <span class="sr-only">GitHub</span>
              <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                <path fill-rule="evenodd"
                  d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"
                  clip-rule="evenodd" />
              </svg>
            </a>
            <a href="https://www.linkedin.com/in/giovannimg/" target="_blank" class="text-gray-400 hover:text-white">
              <span class="sr-only">LinkedIn</span>
              <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                <path
                  d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
              </svg>
            </a>
          </div>
        </div>

        <!-- Secciones -->
        <div class="mt-16 grid grid-cols-2 gap-8 xl:col-span-2 xl:mt-0">
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <h3 class="text-sm font-semibold leading-6 text-white">Navegación</h3>
              <ul class="mt-6 space-y-4">
                <li><a @click="scrollTo('conectar-whatsapp')"
                    class="cursor-pointer text-sm leading-6 text-gray-300 hover:text-white transition-colors">Conectar
                    WhatsApp</a></li>
                <li><a @click="scrollTo('instrucciones-bot')"
                    class="cursor-pointer text-sm leading-6 text-gray-300 hover:text-white transition-colors">Usar el
                    Bot</a></li>
                <li><a @click="scrollTo('panel-administracion')"
                    class="cursor-pointer text-sm leading-6 text-gray-300 hover:text-white transition-colors">Panel de
                    Administración</a></li>
              </ul>
              <ul class="mt-6 space-y-4">
                <li><a @click="scrollTo('instalar-proyecto')"
                    class="cursor-pointer text-sm leading-6 text-gray-300 hover:text-white transition-colors">Instalar
                    Proyecto</a></li>
                <li><a @click="scrollTo('tecnologias')"
                    class="cursor-pointer text-sm leading-6 text-gray-300 hover:text-white transition-colors">Tecnologías</a>
                </li>
              </ul>
            </div>
          </div>
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <h3 class="text-sm font-semibold leading-6 text-white">Contacto</h3>
              <ul class="mt-6 space-y-4">
                <li><a href="mailto:gmolina.dev@gmail.com"
                    class="text-sm leading-6 text-gray-300 hover:text-white transition-colors">gmolina.dev@gmail.com</a>
                </li>
                <li><a href="https://wa.me/353830778954" target="_blank"
                    class="text-sm leading-6 text-gray-300 hover:text-white transition-colors">WhatsApp</a></li>
              </ul>
            </div>
            <div class="mt-10 md:mt-0">
              <h3 class="text-sm font-semibold leading-6 text-white">Repositorios</h3>
              <ul class="mt-6 space-y-4">
                <li><a href="https://github.com/Giovasdf/MVPProyectoTitulo" target="_blank"
                    class="text-sm leading-6 text-gray-300 hover:text-white transition-colors">Frontend</a></li>
                <li><a href="https://github.com/Giovasdf/MVPBackend" target="_blank"
                    class="text-sm leading-6 text-gray-300 hover:text-white transition-colors">Backend</a></li>
                <li><a href="https://github.com/Giovasdf/DATABASE-MVP" target="_blank"
                    class="text-sm leading-6 text-gray-300 hover:text-white transition-colors">Base de Datos</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>


    </div>
  </footer>
</template>

<script setup lang="ts">

// Asegúrate de que el componente o función esté correctamente configurado
const scrollTo = (id: string) => {
  const element = document.getElementById(id)
  if (element) {
    // Desplazamiento suave al elemento con el id
    element.scrollIntoView({ behavior: 'smooth', block: 'start' })
    // Cambia la URL sin recargar la página (mantener el ID en la URL)
    history.replaceState(null, '', `#${id}`)
  }
}
</script>
