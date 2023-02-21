<template>
  <Header :esta_logado="true"></Header>
  <PrimeiroComponente />
  <p class="paragrafo-pai">O dado de App é {{ testando }}</p>
  <life-cycle />
  <pessoa />
</template>

<script lang="ts">
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import LifeCycle from "./components/LifeCycle.vue";
import Pessoa from "./components/Pessoa.vue";
import Header from "./components/Header.vue";
import { defineComponent } from "vue";
export default defineComponent({
  name: "App",
  components: {
    PrimeiroComponente,
    LifeCycle,
    Pessoa,
    Header,
  },
  data() {
    return {
      testando: "Teste",
    };
  },
});
</script>

<style>
body {
  background-color: #333;
  color: #fff;
}

a {
  color: red;
}

.teste {
  background-color: #000;
}
</style>
