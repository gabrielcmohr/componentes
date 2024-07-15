<script setup>
import {ref} from 'vue'

// const props = defineProps(['title', 'content'])

const props = defineProps({
  title: {
    type: String,
    required: true
  },
  content: {
    type: String,
    default: 'Valor padrão de texto da caixa...'
  }
  quantity: {
    type: Number,
      default: 1,
    },
})
const showContent = ref(false)
</script>

<template>
  <div>
    <button @click="showContent = !showContent">Mostrar</button>
    <div v-if="showContent" class="expand-box">
      <h1>{{ props.title }}</h1>
      <p>{{ props.content }}</p>
      <p>{{ props.quantity }}</p>
    </div>
  </div>
</template>

<style scoped>
.expand-box {
  height: 100%;
  padding: 20px;
  border: 1px solid black;
  box-shadow: 2px 2px 3px 3px gray;
  border-radius: 10px;
}
</style>
