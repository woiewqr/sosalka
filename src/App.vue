<script setup lang="ts">
import { ref } from "vue";

const count = ref(0);
function increment() {
    count.value++;
}
function decrement() {
    count.value--;
}
function reset() {
    count.value = 0;
}
</script>

<template>
    <div class="container">
        <h1>Zagubin Sosalka x{{ count }}</h1>
        <div>
            <button @click="increment">Plus Sosalka</button>
            <button @click="decrement">Minus Sosalka</button>
        </div>
        <div>
            <button @click="reset">Reset Sosalku</button>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
}

body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

button {
    background-color: #4caf50;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border: none;
    border-radius: 5px;
}

button:hover {
    background-color: #45a049;
}

button:focus {
    outline: none;
}

button:active {
    background-color: #3e8e41;
}

button:disabled {
    background-color: #ccc;
    color: #666;
    cursor: not-allowed;
}

button:disabled:hover {
    background-color: #ccc;
}

button:disabled:active {
    background-color: #ccc;
}

button:disabled:focus {
    outline: none;
}

h1 {
    font-size: 36px;
    margin-bottom: 20px;
}
</style>
