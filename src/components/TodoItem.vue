<template>
  <div>
    <h2>------- TodoItem Component -------</h2>
    <button @click="deleteTodo">Delete</button>
  </div>
</template>

<script setup>
const props = {
  id: 1,
};

console.log(props, 999);

const emit = defineEmits(["delete"]);

const deleteTodo = () => {
  emit("delete", props.id);
};
</script>
