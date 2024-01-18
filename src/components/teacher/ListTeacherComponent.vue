<template>
  <div>
    <h2>Lista de Profesores</h2>
    <ul>
      <li v-for="(teacher, index) in teachers" :key="index">
        {{ teacher.name }} {{ teacher.subject }} {{ teacher.age }}
      </li>
    </ul>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
    teachers: Array,
})


</script>

