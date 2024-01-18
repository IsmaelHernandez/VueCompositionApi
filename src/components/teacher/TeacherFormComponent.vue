<template>
  <div>
    <h3>Agregar Profesor</h3>
    <form @submit.prevent="submitForm">
      <div>
        <label for="nombre">Nombre:</label>
        <input v-model="form.name" type="text" id="nombre" />
      </div>

      <div>
        <label for="materia">Materia:</label>
        <input v-model="form.subject" type="text" id="materia" />
      </div>

      <div>
        <label for="edad">Edad:</label>
        <input v-model="form.age" type="number" id="edad" />
      </div>

      <button type="submit">Agregar Profesor</button>
      <button @click="resetForm">Resetear Formulario</button>
    </form>

    <ListTeacherComponent :teachers="teachers" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import ListTeacherComponent from './ListTeacherComponent.vue'

const form = ref({
  name: "",
  subject: "",
  age: "",
});

const teachers = ref([]);

const submitForm = () => {
  if (form.value.name && form.value.subject && form.value.age) {
    teachers.value.push({ ...form.value });
    resetForm();
  } else {
    alert("Todos los campos son obligatorios");
  }
};

const resetForm = () => {
  form.value = {
    name: "",
    subject: "",
    age: "",
  };
};
</script>
