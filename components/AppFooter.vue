<script setup lang="ts">
const columns = [
  {
    label: 'Ressources',
    children: [
      { label: 'Starter Kits' },
      { label: 'Release Notes' },
      { label: 'Blog', },
      { label: 'Partners', },
      { label: 'News', },
      { label: 'Jobs', },
      { label: 'Careers', },
    ],
  },
  {
    label: 'Products',
    children: [
      { label: 'Cloud' },
      { label: 'Forge' },
      { label: 'Nightwatch' },
      { label: 'Nova' },
    ]
  },
  {
    label: 'Packages',
    children: [
      { label: 'Cashier' },
      { label: 'Dusk' },
      { label: 'Horizon' },
      { label: 'Octane' },
      { label: 'Scout' },
      { label: 'Pennant' },
      { label: 'Pint' },
    ],
  }
];
</script>

<template>
  <div>
    Component: AppFooter
  </div>
</template>

<style scoped></style>
