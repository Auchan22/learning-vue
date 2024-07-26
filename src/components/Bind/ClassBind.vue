<template>
    <button @click="toggleError()">Cambiar</button>
    <p :class="{danger: hasError}" :style="{...styleObects}">El mensaje se ha enviado satisfactoriamente</p>
</template>

<script lang="ts">
import { defineComponent, StyleValue } from 'vue';

export default defineComponent({
    name: "ClassBind",
    data(){
        let hasError = false;
        let styleObects: StyleValue = {
            fontWeight: "lighter"
        }
        return {hasError, styleObects}
    },
    methods: {
        toggleError(){
            this.hasError = !this.hasError;
            this.styleObects.fontWeight = this.hasError ? "bold" : "lighter";
        }
    }
})
</script>

<style>
.danger {
    color: red;
}
</style>