<template>
  <div class="hello">
    <h1>Hola isma</h1>
    <FirstComponent />
  </div>
</template>

<script>
import FirstComponent from './CounterComponent.vue';
export default {
  name: "HelloWorld",
  components: {
    FirstComponent,
  },
};
</script>
