<template>
  <div>
    <h1>K23</h1>
    <button @click="clicking">Click</button>
  </div>
</template>

<script setup>
const data = "asdasdad";
const emit = defineEmits(["mess"]);
const clicking = () => {
  emit("mess", data);
  // console.log(data);
};
</script>

<style></style>
