<template>
  <div>
    <h2>Dữ liệu trong component con</h2>
    <p>Id : {{ data.prod.id }}</p>
    <p>Product name : {{ data.prod.productName }}</p>
    <p>Price : {{ data.prod.price }}</p>
    <p>Quantity : {{ data.prod.quantity }}</p>
  </div>
</template>

<script setup>
const data = defineProps(["prod"]);
console.log(data);
</script>

<style></style>
