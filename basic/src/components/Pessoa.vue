<template>
  <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
  <Info :email="email" :esta_trabalhando="true" />
  <Form />
</template>

<script lang="ts">
import Info from "./Info.vue";
import Form from "./Form.vue";
import { defineComponent } from "vue";
export default defineComponent({
  name: "Pessoa",
  components: {
    Info,
    Form,
  },
  data() {
    return {
      nome: "Igor",
      email: "igor2@email.com",
    };
  },
});
</script>
