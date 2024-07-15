<script setup>
import { ref, computed } from 'vue'
// defineProps(['title', 'content'])
defineProps({
    title: {
        type: String,
        required: true
    },
    content: {
        type: String,
        default: 'Valor padrão da minha caixa...'
    },
    qty: {
        type: Number,
        default: 9
    },


})
const showBox = ref(false)
const textoBotao = computed(() => showBox.value ? 'Esconder' : 'Mostrar'
) 
</script>

<template>
    <div>
        <button class="butao" @click="showBox = !showBox">
            {{ textoBotao }}
        </button>
        <h3>{{ title }}</h3>
        <div v-if="showBox" class="expand-box">
            <p>{{ content }}</p>
            <p>Quantidade: {{ qty }}</p>
        </div>
    </div>
</template>

<style scoped>
.expand-box {
    height: 100%;
    width: 400px;
    padding: 20px;
    border-radius: 6px;
    border: 1px black solid;
    box-shadow: 3px 3px 2px 2px gray;
}

.butao {
    color: aliceblue;
    height: 22px;
    background-color: rgb(43, 43, 43);
    border-radius: 8px;
    border: 1px solid rgb(0, 0, 0);
}

h3 {
    color: brown;
}
</style>