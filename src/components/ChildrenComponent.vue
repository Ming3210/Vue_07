<template>
  <div>
    <b>----- Children Component -----</b>
    <p>Children company : {{ props.company }}</p>
  </div>
</template>

<script setup>
const props = defineProps(["company"]);
console.log(props);
</script>

<style></style>
