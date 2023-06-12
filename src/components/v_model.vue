<template>
  <input v-model="message" type="text" />
  <p>{{ message }}</p>

  <div v-if="isVisible">
    <p>This element is visible.</p>
  </div>
  <div v-else>
    <p>This element is hidden.</p>
  </div>

  <ul>
    <li v-for="item in items" :key="item.id">
      {{ item.name }}
    </li>
  </ul>

  <img v-bind:src="imageSrc" alt="Vue.js Logo" />

  <button v-on:click="incrementCounter">Click me</button>
</template>

<script lang="ts" setup>
import { ref } from "vue";
const message = ref("");
const isVisible = ref(true);
interface Item {
  id: number;
  name: string;
}

const items = ref<Item[]>([
  { id: 1, name: "Item 1" },
  { id: 2, name: "Item 2" },
  { id: 3, name: "Item 3" },
]);
const imageSrc = ref("https://www.gstatic.com/webp/gallery/2.jpg");
const incrementCounter = () => {
  // Logic to increment the counter
};
</script>
