<template>
  <h1>Mi primer componente compositionAPI</h1>
  <h3>{{ count }}</h3>
  <button @click="increment">Increment</button>
  <button @click="decrement">Decrement</button>
  <button @click="reset">Reset</button>
</template>

<script setup>
import { ref } from "vue";

const count = ref(0);

const increment = () => {
  count.value++;
};

const decrement = () => {
  count.value = count.value - 1;
};

const reset = () => {
  count.value = 0;
};
</script>
