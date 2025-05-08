<template>
  <header class="bg-white dark:bg-gray-800 fixed w-full z-10 top-0 shadow">
    <nav class="mx-auto flex max-w-7xl items-center justify-between p-4 lg:px-8" aria-label="Global">
      <!-- Logo -->
      <div class="flex lg:flex-1 items-center">
        <a href="#" class="flex items-center gap-x-2">
          <IconMediBot />
          <span class="text-lg font-bold text-indigo-600 dark:text-indigo-400">MediBot</span>
        </a>
      </div>

      <!-- Botón del menú móvil -->
      <div class="flex lg:hidden">
        <button @click="mobileMenuOpen = true" type="button"
          class="inline-flex items-center justify-center rounded-md p-2 text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
          <span class="sr-only">Abrir menú</span>
          <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>
      </div>

      <!-- Menú de escritorio -->
      <div class="hidden lg:flex lg:gap-x-12">
        <a v-for="item in navItems" :key="item.id" href="javascript:void(0)" @click="scrollToSection(item.id)"
          class="text-sm font-semibold leading-6 text-gray-900 dark:text-white hover:text-indigo-500">
          {{ item.label }}
        </a>
      </div>
    </nav>

    <!-- Menú móvil -->
    <div v-if="mobileMenuOpen" class="lg:hidden" role="dialog" aria-modal="true">
      <div class="fixed inset-0 z-10 bg-black bg-opacity-50" @click="mobileMenuOpen = false"></div>
      <div
        class="fixed inset-y-0 right-0 z-20 w-3/4 max-w-sm bg-white dark:bg-gray-800 px-6 py-6 overflow-y-auto shadow-lg">
        <div class="flex items-center justify-between">
          <a href="#" class="flex items-center gap-x-2">
            <IconMediBot />
            <span class="text-lg font-bold text-indigo-600 dark:text-indigo-400">MediBot</span>
          </a>
          <button @click="mobileMenuOpen = false" type="button"
            class="rounded-md p-2 text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
            <span class="sr-only">Cerrar menú</span>
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
        <div class="mt-6 space-y-4">
          <a v-for="item in navItems" :key="item.id" href="javascript:void(0)"
            @click="scrollToSection(item.id); mobileMenuOpen = false"
            class="block text-base font-semibold text-gray-900 dark:text-white hover:text-indigo-500">
            {{ item.label }}
          </a>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref, defineComponent } from 'vue'

// Estado del menú móvil
const mobileMenuOpen = ref(false)

// Navegación dinámica
const navItems = [
  { id: 'conectar-whatsapp', label: 'Conectar WhatsApp' },
  { id: 'instrucciones-bot', label: 'Usar el Bot' },
  { id: 'panel-administracion', label: 'Panel de Administración' },
  { id: 'instalar-proyecto', label: 'Instalar Proyecto' },
  { id: 'tecnologias', label: 'Tecnologías' },
]

// Scroll suave
function scrollToSection(id: string): void { // Se agrega el tipo string
  const el = document.getElementById(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}

// Componente de ícono en línea
const IconMediBot = defineComponent({
  name: 'IconMediBot',
  template: `
    <svg class="h-8 w-8 text-indigo-500 dark:text-indigo-400" fill="currentColor" viewBox="0 0 24 24">
      <path d="M12 2L2 7v10l10 5 10-5V7L12 2zm0 2.8L20 9v6l-8 4-8-4V9l8-4.2z" />
      <path d="M12 15c-1.1 0-2-.9-2-2s.9-2 2-2 2 .9 2 2-.9 2-2 2z" />
    </svg>
  `
})
</script>
