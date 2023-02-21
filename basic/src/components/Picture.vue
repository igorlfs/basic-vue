<template>
  <div>
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @mudar-imagem="trocarImagem" />
  </div>
</template>

<script lang="ts">
import MudarImagem from "./MudarImagem.vue";
import { defineComponent } from "vue";
export default defineComponent({
  name: "Picture",
  components: {
    MudarImagem,
  },
  data() {
    return {
      avatar: "/img/avatar.jpg",
      descricao: "Squid",
    };
  },
  methods: {
    trocarImagem() {
      this.avatar = "/img/manga.png";
    },
  },
});
</script>
