<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <v_model msg="Welcome to Your Vue.js + TypeScript App" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import v_model from "./components/v_model.vue";

export default defineComponent({
  name: "App",
  components: {
    v_model,
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
