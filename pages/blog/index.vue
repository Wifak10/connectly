<script setup lang="ts">
const {data:posts} = await useAsyncData('posts',()=> queryCollection('blog').all());

</script>

<template>
    <!-- <div>
         <p v-if="posts"> on a {{ posts?.length }} posts </p>
    </div> -->
    <UContainer>
        <UBlogList>
            <UBlogPost v-for="post in posts" 
            :key="post.id" 
            :title="post.title"
            :description="post.description"
            :image="post.image"
            :auteurs="post.auteurs"
            />
        </UBlogList>

    </UContainer>

</template>

<style scoped></style>