<!-- CountParent.vue -->
<template>
  <div>
    <h1>B3</h1>
    <p>Count: {{ count }}</p>
    <CountChildren @increase="handleIncrease" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import CountChildren from "./CountChildren.vue";

const count = ref(0);

const handleIncrease = () => {
  count.value++;
};
</script>
