<template>
  <div>
    parents
    <div>
      <Child :default="{ item }" :propsName="message" :age="age">
        <template #mmb><h2>MMB</h2></template>
        <template #mbb><h2>MMB</h2></template>
        <h2>MBB</h2>
      </Child>
      <p>Gía trị nhận về từ cha ;{{ item }}</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Child from "./Child.vue";
const message = ref("aw");
let age = ref(22);
</script>

<style></style>
