<template>
    <h3>Contador con Option API</h3>
    <div class="contador-wrapper">
        <button class="btn" @click="decrement()" :disabled="count == 0 ">-</button>
        <p>{{ count }}</p>
        <button  class="btn" @click="increment()">+</button>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

interface DataProps {
    count: number;
}

export default defineComponent({
    name: "CounterOption",
    data(): DataProps{
        return {
            count: 0
        }
    },
    methods:{
        increment(): void{
            this.count++;
        },
        decrement(): void {
            if(this.count > 0){
                this.count--;
            }
        }
    }
})
</script>

<style scoped>
    .contador-wrapper {
        display: flex;
        gap: 10px;
        align-items: center;
        justify-content: center;
    }
    .btn {
        background-color: #000;
        color: #fff;
        border: none;
        border-radius: 15px;
        padding: 10px 15px;
    }
    .btn:disabled{
        opacity: 0.4;
    }
    .btn:hover:not(:disabled){
        cursor: pointer;
        box-shadow: 1px 1px 1px 1px #8d8d8d;
    }
</style>