<script setup>
import ExpandBox from './components/ExpandBox.vue'
import Card from './components/Card.vue'
import CardFull from './components/CardFull.vue';

const caixas = [
  { id: 1, title: 'Caixa 1', content: 'conteúdo 1', qty: 100 },
  { id: 2, title: 'Caixa 2', qty: 30 },
  { id: 3, title: 'Caixa 3', content: 'conteúdo 3' },
  { id: 4, title: 'Caixa 4' }
]
</script>

<template>
  <h1>Componentes</h1>
  <hr>

  <h2>AULA 1 - Box</h2>
  <ExpandBox v-for="caixa in caixas" :key="caixa.id" v-bind="caixa"></ExpandBox>
  <!-- <ExpandBox title="Bola"/>
  <expand-box title="Quadrado" qty="26478"/>
  -->

  <h2>AULA 2 - Card</h2>
  <div>
    <Card title="Lamine YAMAL">
      <p>Lamine Yamal is the best young football player since Neymar Junior?</p>
    </Card>
    <br>
    <Card title="Card 2"></Card>
  </div>
  <h2>CardFull</h2>
  <div>
    <Card>
      <p>Body</p>
      <template #header>
        <h1>Header</h1>
      </template>
      <template #footer>
        <p>Footer</p>
      </template>
    </Card>
  </div>
</template>

<style scoped></style>
