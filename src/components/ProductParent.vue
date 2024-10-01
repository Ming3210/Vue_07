<template>
  <div>
    <h1>B2</h1>
    <ProductChildren :prod="data" />
  </div>
</template>

<script setup>
import ProductChildren from "./ProductChildren.vue";
const data = {
  id: 1,
  productName: "Bưởi Ba Roi",
  price: "12000đ",
  quantity: 10,
};
</script>

<style></style>
