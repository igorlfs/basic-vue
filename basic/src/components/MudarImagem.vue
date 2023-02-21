<template>
  <div>
    <button @click="$emit('mudarImagem')">Trocar imagem de perfil</button>
  </div>
</template>

<script lang="ts">
export default {
  name: "MudarImagem",
  emits: ["mudarImagem"],
};
</script>
