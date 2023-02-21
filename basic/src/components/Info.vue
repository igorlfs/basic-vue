<template>
  <p>{{ email }}</p>
  <p v-if="esta_trabalhando">Estou trablhando no momento.</p>
  <p v-else>Estou em busca de novas oportunidades!</p>
  <p>Utilizo as seguintes tecnologias para back-end:</p>
  <ul>
    <li v-for="tech in backend_tech">
      {{ tech }}
    </li>
  </ul>
  <p>Utilizo as seguintes tecnologias para front-end:</p>
  <ul>
    <li v-for="tech in frontnd_tech">{{ tech.language }}</li>
  </ul>
  <div>
    <button @click="showEmail">{{ texto_botao }}</button>
  </div>
  <p v-show="mostar_email">Mande uma mensagem para: {{ email }}</p>
  <p class="teste">
    Para acessar meu portfólio basta clicar aqui:
    <a v-bind:href="meu_link" target="_blank"> basta clicar aqui </a>
  </p>
  <Picture />
</template>

<script lang="ts">
import Picture from "./Picture.vue";
import { defineComponent } from "vue";
export default defineComponent({
  name: "Info",
  components: {
    Picture,
  },
  props: {
    email: String,
    esta_trabalhando: Boolean,
  },
  data() {
    return {
      mostar_email: false,
      meu_link: "https://google.com",
      texto_botao: "Mostrar e-mail",
      backend_tech: ["JavaScript", "PHP", "Python"],
      frontnd_tech: [
        {
          id: 1,
          language: "HTML",
        },
        {
          id: 2,
          language: "CSS",
        },
        {
          id: 3,
          language: "Vue",
        },
      ],
    };
  },
  methods: {
    showEmail() {
      this.mostar_email = !this.mostar_email;
      if (!this.mostar_email) {
        this.texto_botao = "Mostrar e-mail";
      } else {
        this.texto_botao = "Esconder e-mail";
      }
    },
  },
});
</script>

<style>
.paragrafo-pai {
  color: red;
}
</style>
