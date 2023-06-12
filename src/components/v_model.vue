<template>
  <input v-model="message" type="text" />
  <p>{{ message }}</p>
</template>

<script lang="ts" setup>
import { ref } from "vue";
const message = ref("");
</script>
