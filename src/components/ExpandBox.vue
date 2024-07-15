<script setup>
import { ref, computed } from 'vue'
// defineProps(['title', 'content', 'nome']);
defineProps({
  title: {
    type: String,
    required: true
  },
  content: {
    type: String,
    default: "valor padrão da minha caixa..."
  },
  qtd: {
    type: Number,
    default: 10
  }
})
const ShowBox = ref(false);
const textBotao = computed(() => (ShowBox.value ? 'Esconder' : 'Mostrar'));
</script>

<template>
  <div>
  <button @click="ShowBox = !ShowBox">
    {{ textBotao }}
  </button>

  <div v-if="ShowBox" class="expand-box">
    <h1>{{ title }}</h1>
    <p>{{ content }}</p>
    <p> quantidade: {{ qtd }}</p>

  </div>
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
