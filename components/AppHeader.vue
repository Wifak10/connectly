<script setup lang="ts">
import AsideLinks from '@nuxt/ui-pro/components/aside/AsideLinks.vue';

const items = [
  {
    label: 'Blog',
    to:'/blog',
  },
  {
    label: 'A propos',
    to:'/about',
  },
]
</script>

<template>
  <UHeader>
    <template #left>
      <NuxtLink to="/">
        <img src="/assets/logo.png" alt="logo de connectly" class="w-auto h-6 shrink-8"/>
      </NuxtLink>
    </template>

    <template #center>
      <UHeaderLinks :links="items" />

       <UVisibility :visible="true" :breakpoint="'sm'">
        <UHeaderLinks :links="items" />
      </UVisibility>
      

    </template>

    <template #right>
      <UButton label="Se connecter" variant="link" color="orange" to="/login" /> 
      <UColorModeButton /> 
    </template>
  </UHeader>

  <UHeader>
    <template #panel>
      <UAsideLinks :links="items" />
    </template>
  </UHeader>
</template>

<style scoped></style>
