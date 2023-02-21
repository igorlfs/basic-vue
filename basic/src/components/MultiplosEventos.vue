<template>
  <div>
    <button @click="primeiro('primeiro evento'), segundo('segundo evento')">
      Ativar múltiplos eventos
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script lang="ts">
export default {
  name: "MultiplosEventos",
  data() {
    return {
      multiplos_eventos: "",
    };
  },
  methods: {
    primeiro(txt: string) {
      this.multiplos_eventos = txt;
    },
    segundo(txt: string) {
      setTimeout(() => (this.multiplos_eventos = txt), 500);
    },
  },
};
</script>

<style scoped>
div {
  margin: 100px;
}
</style>
