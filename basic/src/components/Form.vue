<template>
  <h2>Meu formulário:</h2>
  <form action="" @submit.prevent="enviarFormulario($event)">
    <div>
      <input type="text" v-model="name" />
    </div>
    <div>
      <input type="text" v-model="email" />
    </div>
    <div>
      <Submit />
    </div>
  </form>
  <p>Conteúdo</p>
  <p>Conteúdo</p>
  <p>Conteúdo</p>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import InputText from "./form/InputText.vue";
import Submit from "./form/Submit.vue";
export default defineComponent({
  name: "Form",
  components: {
    InputText,
    Submit,
  },
  data() {
    return {
      name: "",
      email: "",
    };
  },
  methods: {
    enviarFormulario(e: Event) {
      // Não funcionaaaaaaaaaaaaa
      e.preventDefault();
      const name = this.name;
      const email = this.email;

      console.log("Formulário enviado");
      console.log("O nome é " + name);
      console.log("O nome é " + email);
    },
  },
});
</script>

<style scoped>
p {
  margin: 50px;
}
</style>
