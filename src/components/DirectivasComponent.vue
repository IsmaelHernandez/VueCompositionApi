<template>
  <div>
    <h1>Directivas Selectivas (Renderizado condicional)</h1>
  </div>
  <!-- Se puede utilizar la etiqueta <template> para indicar un bloque condicional 
    que contiene solo texto o varios elementos. -->
  <template v-if="age < 18">
    <h2>Eres menor de edad</h2>
  </template>
  <template v-else>
    <h3>Eres mayor de edad</h3>
  </template>
  <br />
  <div></div>
  <div>
    <h1>Directivas v-for (recorrido de archivos)</h1>
    <ul>
      <li v-for="item in books" :key="item">
        {{ item.code }}, {{ item.name }}
      </li>
    </ul>
    <p :class="{'danger' : hasError}">El mensaje sea enviado correctamente</p>
  </div>
</template>

<script setup>
import { ref } from "vue";

const age = ref(18);

let hasError = ref(false);

const books = ref([
  {
    code: "es",
    name: "spain",
  },
  {
    code: "en",
    name: "UK",
  },
  {
    code: "eu",
    name: "EUA",
  },
]);
</script>

<style>
h2 {
  color: burlywood;
}
h3 {
  color: green;
}

.danger {
    color: red;
}
</style>
