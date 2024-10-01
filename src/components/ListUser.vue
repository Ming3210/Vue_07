<template>
  <div class="list-user">
    <h1>B8</h1>
    <h2>------- List User -------</h2>
    <button @click="showForm" class="add-user-btn">Add user</button>
    <form-add-user v-if="isFormVisible" @close="hideForm"></form-add-user>
  </div>
</template>

<script setup>
import { ref } from "vue";
import FormAddUser from "./FormAddUser.vue";

const isFormVisible = ref(false);

const showForm = () => {
  isFormVisible.value = true;
};

const hideForm = () => {
  isFormVisible.value = false;
};
</script>

<style scoped>
.add-user-btn {
  background-color: #0062ff;
  border: none;
  color: white;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 4px;
}
</style>
