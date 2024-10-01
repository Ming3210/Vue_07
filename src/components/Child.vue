<template>
  <div>
    child
    <p>Giá trị nhận về : {{ props.propsName }}</p>
    <p>Tuổi : {{ props.age }}</p>
    <p>mmb</p>
    <slot name="mmb"></slot>

    <slot :item="data" name="mbb"></slot>
    <p>mbb</p>
  </div>
</template>

<script setup>
const data = "datatatatatatatatatatatatatatatatatatatat";
// const props = defineProps([ propsName: "123" ]);
const props = defineProps({ propsName: "123", age: "" });
console.log(props.propsName);
</script>

<style></style>
