<template>
    <div class="post-container">
        <PostCard v-for="(post, index) in posts" :key="index" :data="post"/>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PostCard from './PostCard.vue';
import { Post } from '@/interfaces/Post.interface';

export default defineComponent({
    name: "PostWrapper",
    components: {
        PostCard
    },
    data(): {posts: Post[]}{
        return {
            posts: [
                {title: "Titulo 1", description: "prueba"},
                {title: "Titulo 2", description: "prueba 2"},
                {title: "Titulo 3", description: "prueba 3"},
                {title: "Titulo 4", description: "prueba 4"},
            ]
        }
    }
})
</script>

<style scoped>
    .post-container {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
    }
</style>