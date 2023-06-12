<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <v_directives msg="Welcome to Your Vue.js + TypeScript App" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import v_directives from "./components/v_directives.vue";

export default defineComponent({
  name: "App",
  components: {
    v_directives,
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
