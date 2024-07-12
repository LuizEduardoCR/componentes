<script setup>
import { ref, computed } from 'vue'
const props = defineProps(['title', 'content', 'nome']);
const ShowBox = ref(false);
const textBotao = computed(() => (ShowBox.value ? 'Esconder' : 'Mostrar'));
</script>

<template>
  <button @click="ShowBox = !ShowBox">
    {{ textBotao }}
  </button>

  <div v-if="ShowBox" class="expand-box">
    <h1>{{ props.title }}</h1>
    <p>{{ props.content }}</p>
    <p>{{ props.nome }}</p>
  </div>
</template>

<style scoped>
.expand-box {
  height: 100%;
  width: 400px;
  padding: 20px;
  border-radius: 10px;
  border: black 1px solid;
  box-shadow: 3px 3px 2px 2px grey;
}
</style>
