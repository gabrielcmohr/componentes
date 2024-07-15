<script setup>
import ExpandBox from './components/ExpandBox.vue'
const caixas = [
  { id: 1, title: 'Caixa 1', content: 'Conteúdo 1', quantity: 100 },
  { id: 2, title: 'Caixa 2'},
  { id: 3, title: 'Caixa 3', quantity: 50 },
  { id: 4, title: 'Caixa 4', content: 'conteúdo secreto 4'},

]
</script>

<template>
  <h1>Componentes</h1>
  <expand-box v-for="caixa in caixas" :key="caixa.id" v-bind:="caixa" />
  <!--<ExpandBox title="Caixa 1" content="Conteúdo secreto 1"/>
  <ExpandBox title="Caixa 2" />
  <Expand-box title="Caixa 3"/> -->
</template>

<style scoped></style>
