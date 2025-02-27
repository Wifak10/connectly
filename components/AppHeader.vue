<script setup lang="ts">
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
        <!-- <UHeading>My Blog</UHeading> -->
      </NuxtLink>
    </template>

    <template #center>
      <UNavigationLinks :links="items" /> 
    </template> 
    

    <template #right> 
      <UButton label="Se connecter" variant="link" color="orange" to="/login" /> 
      <UColorModeButton /> 
    </template>
  </UHeader>
</template>

<style scoped></style>
