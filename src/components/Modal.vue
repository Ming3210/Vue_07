<template>
  <div v-if="isOpen" class="modal">
    <div class="modal-content">
      <div class="modal-header">
        <slot name="header">
          <h3>Modal Title</h3>
        </slot>
        <button class="close-btn" @click="closeModal">X</button>
      </div>
      <div class="modal-body">
        <slot> Modal body content </slot>
      </div>
      <div class="modal-footer">
        <button class="close-btn" @click="closeModal">Close</button>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  isOpen: {
    status: false,
  },
});

const emit = defineEmits(["close"]);

const closeModal = () => {
  emit("close");
};
</script>

<style>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  background-color: #fff;
  padding: 20px;
  border-radius: 4px;
  width: 300px;
  text-align: center;
}

.modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.close-btn {
  background-color: #ccc;
  border: none;
  padding: 5px 10px;
  cursor: pointer;
}

.modal-body {
  margin: 20px 0;
}
</style>
