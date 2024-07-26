<template>
    <div class="post-card">
        <h3>{{ data.title }}</h3>
        <p>{{ data.description ? data.description : "<i>Sin descripción</i>" }}</p>
        <PostButton />
    </div>

</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import PostButton from './PostButton.vue';
import { Post } from '@/interfaces/Post.interface';

export default defineComponent({
    name: "PostCard",
    components: {
        PostButton
    },
    props: {
        data: {type: Object as PropType<Post>, required: true}
    }
})
</script>

<style scoped>
    .post-card {
        border-radius: 15px;
        padding: 10px;
        margin: 5px;
        border: 1px solid #ccc;
    }
</style>