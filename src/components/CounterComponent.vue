<template>
  <h1>{{ count }}</h1>
  <button @click="increment">Increment</button>
  <button @click="decrement">Decrement</button>
  <button @click="reset">Reset</button>
</template>

<script setup>

import { ref } from "vue";

const count = ref(0); //propiedad que hago reactiva

const increment = () => {
  return count.value++;
};

const decrement = () => {
  return (count.value = count.value - 1);
};

const reset = () => {
  return (count.value = 0);
};


</script>
