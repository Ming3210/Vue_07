<template>
  <div>
    <h1>B7</h1>
    <MessageChildren @send-message="showNotification"></MessageChildren>
  </div>
</template>

<script setup>
import MessageChildren from "./MessageChildren.vue";

const showNotification = (message) => {
  if (message) {
    alert("Nice");
  }
};
</script>

<style scoped>
.notification {
  background-color: #333;
  color: white;
  padding: 15px;
  margin-top: 20px;
  border-radius: 5px;
}
</style>
