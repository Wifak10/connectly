<script setup lang="ts">
import {useBreakpoints } from '@vueuse/core'

//On use les breakpoints pour définir les tailles de l'écran possible
const breakpoints = useBreakpoints({
  mobile: 0, // optional
  tablet: 640,
  laptop: 1024,
  desktop: 1280,
  lg: 100000,
})
 
//Vérifier si la taille de l'écran actuelle est parmi les tailles renseigné
const laptop = breakpoints.between('laptop', 'lg')

const links = [
  {
    label:'Blog',
    to:'/blog',
  },
  {
    label:'A propos',
    to:'/about',
  }
];
</script>

<template>
  <UHeader>
    <template #left>
      <NuxtLink to="/">
        <img src="/logo.png" alt="Logo de Connectly" class="w-auto h-6 shrink-0">
      </NuxtLink>
    </template>

    <template #center v-if="laptop">
      <UHeaderLinks  :links="links" />
    </template>
    
    <template #right>
      <UButton label="Se connecter" variant="solid" color="orange"/>
      <UColorModeButton/>
    </template>

    <template #panel>
      <UHeaderPopoverLinks :links="links" />
    </template>
  </UHeader>
</template>

<style scoped>

</style>
