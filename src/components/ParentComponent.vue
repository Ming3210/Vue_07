<template>
  <div>
    <h1>B1</h1>
    <b>----- Parent Company -----</b>
    <p>Parent Company : {{ company }}</p>
    <ChildrenComponent :company="company" />
  </div>
</template>

<script setup>
import { ref } from "vue";
const company = ref("Rikkei Academy");
import ChildrenComponent from "./ChildrenComponent.vue";
</script>

<style></style>
