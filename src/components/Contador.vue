<template>
  <div style="display: flex">
    <button @click="decremento">Decrementar</button>
    <p>{{ contador }}</p>
    <button @click="incremento">Incrementar</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const contador = ref(0);

const incremento = () => {
  //.value es la forma en la que cambiamos los valores de una variable reactiva u obtener su valor
  contador.value++;
};
const decremento = () => {
  //.value es la forma en la que cambiamos los valores de una variable reactiva u obtener su valor
  contador.value--;
};
</script>

<style scoped>
p {
  color: red;
  padding: 20px;
  font-size: 10px;
}
</style>
