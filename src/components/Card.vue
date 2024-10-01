<template>
  <div class="card">
    <div class="card-header">
      <slot name="header">Default Header</slot>
    </div>
    <div class="card-body">
      <slot>Default Body</slot>
    </div>
    <div class="card-footer">
      <slot name="footer">Default Footer</slot>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.card {
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 20px;
  max-width: 400px;
  box-shadow: 0px 2px 8px rgba(0, 0, 0, 0.1);
}

.card-header {
  font-weight: bold;
  font-size: 18px;
  margin-bottom: 10px;
}

.card-body {
  font-size: 16px;
  margin-bottom: 20px;
}
</style>
