<template>
  <div>
    <button @click="sendMessage">Send message</button>
  </div>
</template>

<script setup>
import { defineEmits } from "vue";

const emit = defineEmits(["send-message"]);

const sendMessage = () => {
  emit("send-message", true);
};
</script>
