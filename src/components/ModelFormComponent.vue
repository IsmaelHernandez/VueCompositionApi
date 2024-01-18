<template>
    <h1>Formularios en vue.js 3</h1>
   <form action="">
    <label for=""></label>
    <input type="text" v-model="inputTex">
    <h3>{{ inputTex }}</h3>
   </form>
</template>

<script setup>
import { ref } from 'vue';

let inputTex = ref('')

</script>