<template>
  <h1>Meu nome é: {{ exemplo }}</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "LifeCycle",
  data() {
    return {
      exemplo: "Ainda não sei",
    };
  },
  created() {
    setTimeout(() => {
      this.exemplo = "Igor";
    }, 1000);

    this.lifeCycle();
  },
  mounted() {
    setTimeout(() => {
      this.exemplo = "Pedro";
    }, 2000);
  },
  methods: {
    lifeCycle() {
      console.log("Executou");
    },
  },
});
</script>
