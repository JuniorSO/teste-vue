<script lang="ts" setup>
const count = ref(0);
const toOneHundred = computed(() => 100 - count.value);

function sumCounter() {
  count.value += 1;
}
</script>

<template>
  <div>
    <h1>{{ count }}</h1>
    <button @click="sumCounter()">Contador</button>
    <span>Para atingir 100, faltam {{ toOneHundred }} cliques!</span>
  </div>
</template>

<style scoped>
* {
  font-family: sans-serif;
  padding: 0;
  margin: 0;
}

h1 {
  color: blueviolet;
}

button {
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
}
</style>
