<script setup lang="ts">
const {data: homepage} = await useAsyncData(() => queryCollection('webpages').path('/').first())

</script>


<template>

<div>Page Blog</div>
<div>
    <ContentRenderer v-if="homepage" :value="homepage" />
</div>
</template>


<style scoped>


</style>