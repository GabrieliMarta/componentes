<script setup>
import { ref, computed } from 'vue';
//const props = defineProps(['title', 'content'])
const props = defineProps({
    title: {
        type: String,
        required: true 
    },
    content:{
        type: String,
        default: "Valor padrão do texto da caixa..."

    
    }, quantity:{
        type:Number,
        default: 1,
    }
})
const showContent = ref(false)
const textButton = computed(() => ( showContent.value ? 'Esconder' : 'Mostrar'))
</script>

<template>
    <div><button @click="showContent = !showContent">{{ textButton }}</button>
        <div v-if="showContent" class="expand-box">beijinho no ombro
            <h1>{{ title }}</h1>
            <p>{{ content }}</p>
            <p>Quantidade: {{ quantity }}</p>
        </div>
    </div>
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
