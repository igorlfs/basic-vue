<template>
  <div class="main-container">
    <h1>Gerenciar Pedidos</h1>
    <Dashboard></Dashboard>
  </div>
</template>

<script lang="ts">
import Dashboard from "../components/Dashboard.vue";
export default {
  name: "Pedidos",
  components: {
    Dashboard,
  },
};
</script>
