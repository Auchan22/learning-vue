<template>
    <button class="post-btn">ACCEDER</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: "PostButton",
})
</script>

<style scoped>
    .post-btn {
        padding: 15px;
        background-color: blueviolet;
        border-radius: 10px;
        color: #fff;
        border: 0;
        outline: 0;
        transition: all 125ms ease-in-out;
    }

    .post-btn:hover {
        background-color: #fff;
        color: blueviolet;
        font-weight: bold;
        cursor:pointer;
        background-color: #e3e3e3;
    }
</style>