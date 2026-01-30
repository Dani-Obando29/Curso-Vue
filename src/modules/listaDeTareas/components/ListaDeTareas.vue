<template>
  <div>
    <h2>Lista de Tareas</h2>
    <!-- v-model es una variable reactiva que se asgina -->
    <input type="text" v-model="nuevaTarea" @keyup.enter="addTask" />
    <ul>
      <!-- v-for es para crear un foreach dentro de la etiqueta -->
      <li v-for="(tareas, index) in tareas" ::key="index">
        <!-- {{ tareas }} permite mostrar variables  -->
        {{ tareas }}
        <button @click="borrarTarea">Eliminar</button>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";
const tareas = ref([]);
const nuevaTarea = ref("");
const addTask = () => {
  tareas.value.push(nuevaTarea.value); //este es el array
  nuevaTarea.value = "";
};

const borrarTarea = (index) => {
  tareas.value.splice(index, 1);
};
</script>

<style scoped></style>
