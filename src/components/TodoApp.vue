<template>
  <div>
    <h2>------- TodoApp Component -------</h2>
    <p>Id to delete: {{ idToDelete }}</p>
    <TodoItem @delete="handleDelete" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import TodoItem from "./TodoItem.vue";

const idToDelete = ref(null);

const handleDelete = (id) => {
  idToDelete.value = id;
};
</script>
