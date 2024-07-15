<script setup>
import { ref } from 'vue';
const showContent = ref(false)
</script>

<template>
    <div><button @click="showContent = !showContent">mostrar</button></div>
    <div v-if="showContent" class="expand-box">beijinho no ombro</div>
</template>

<style scoped>
.expand-box {
    height: 80%;
    padding: 20px;
    border: 1 px solid black;
    box-shadow: 2px 2px 3px 2px gray;
    border-radius: 10px;
}
</style>
