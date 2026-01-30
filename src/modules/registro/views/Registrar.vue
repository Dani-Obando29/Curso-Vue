<!-- Template -->
<template>
  <div>
    <h2>Formulario de Registro</h2>
    <Form :validation-schema="schema" @submit="onSubmit">
      <div class="form">
        <label for="nombre">Nombre:</label>
        <Field type="text" name="nombre" id="nombre" placeholder="Ingrese su nombre" />
        <ErrorMessage name="nombre"></ErrorMessage>
      </div>
      <div class="form">
        <label for="correo">Email:</label>
        <Field type="email" name="email" id="correo" placeholder="email@example.com" />
        <ErrorMessage name="email"></ErrorMessage>
      </div>
      <div class="form">
        <button type="submit">Registrar</button>
      </div>
    </Form>
  </div>
</template>

<!-- script -->
<script setup>
import { Form, Field, ErrorMessage } from "vee-validate";
import { schema } from "../schemas/validationSchema";

const onSubmit = () => {
  alert("se ha enviado el formulario");
};
</script>

<!-- Style -->
<style scoped>
.form {
  margin-bottom: 10px;
}
</style>
