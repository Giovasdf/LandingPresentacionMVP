<template>
  <div class="bg-gray-950 text-white min-h-screen relative">
    <NavbarComponent />
    <HeroComponent id="inicio" />
    <WhatsAppConnectComponent id="conectar-whatsapp" />
    <WhatsAppInstructionsComponent id="instrucciones-bot" />
    <FrontEndInstructionsComponent id="panel-administracion" />
    <ProjectInstructionsComponent id="instalar-proyecto" />
    <TechonologyListComponent id="tecnologias" />
    <SiteFooterComponent />
  </div>
</template>

<script lang="ts" setup>
import NavbarComponent from '../components/NavbarComponent.vue'
import HeroComponent from '../components/HeroComponent.vue'
import WhatsAppConnectComponent from '../components/WhatsAppConnectComponente.vue'
import WhatsAppInstructionsComponent from '../components/WhatsAppInstructionsComponent.vue'
import FrontEndInstructionsComponent from '../components/FrontEndInstructionsComponent.vue'
import TechonologyListComponent from '../components/TechonologyListComponent.vue'
import ProjectInstructionsComponent from '../components/ProjectInstructionsComponent.vue'
import SiteFooterComponent from '../components/SiteFooterComponent.vue'
</script>
