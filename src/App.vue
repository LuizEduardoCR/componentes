<script setup>
import CardFull from './components/CardFull.vue'
  import Card from './components/Card.vue';
import ExpandBox from './components/ExpandBox.vue';
const caixas=[
    {id: 1, title:'caixa 1', content: 'conteudo1', qtd: 100},
    {id: 2, title:'caixa 2', qtd: 100},
    {id: 3, title:'caixa 3', content: 'conteudo 3'},
    {id: 4, title:'caixa 4' }
]
</script>

<template>
    <h1>Componentes</h1>
    <h2>Props</h2>
    <hr>
    <div>
    <Card title="Card 1">
        <h2>meu subtitulo</h2>
        <p>Conteúdo do card</p>
    </Card>
  </div>
  <div>
    <card title="Card 2 ">
    </card>
    <CardFull>
      <p>Body</p>
      <h2>meu dados</h2>
      <template #header>
        <h1>Header</h1>
        <h2>meu nome</h2>
      </template>
     <!-- <template #footer>
        <p>Footer</p>
      </template>-->
    </CardFull>
  </div>

<hr>
<!--<expand-box v-for="caixa in caixas" :key="caixa.id" v-bind="caixa"/>
<ExpandBox title="Caixa 1"  content="conteudo secreto da caixa 1" />
<br>
<expand-box title="Caixa 2" qtd="50"/>-->
</template>

<style scoped>

</style>
