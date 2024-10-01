<!-- CountChildren.vue -->
<template>
  <div>
    <button @click="increasing">Increase</button>
  </div>
</template>

<script setup>
const emit = defineEmits(["increase"]);
const increasing = () => {
  emit("increase");
};
</script>
