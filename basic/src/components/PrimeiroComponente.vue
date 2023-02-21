<template>
  <Reutilização />
  <h1>Olá Vue!</h1>
  <Reutilização />
  <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
  <MultiplosEventos />
  <Reutilização />
  <Reutilização />
  <Reutilização />
  <Reutilização />
</template>

<script lang="ts">
import MultiplosEventos from "./MultiplosEventos.vue";
import Reutilização from "./Reutilização.vue";
export default {
  name: "PrimeiroComponente",
  components: {
    MultiplosEventos,
    Reutilização,
  },
  data() {
    return {
      nome: "Igor",
      profissao: "programador",
    };
  },
};
</script>
