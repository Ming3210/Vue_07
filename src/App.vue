<template>
  <div>
    <ParentComponent></ParentComponent>
    <ProductParent />
    <CountParent />
    <TodoApp />
    <div>
      <h1>B5</h1>
      <button @click="openModal">Open Modal</button>

      <Modal :isOpen="isModalOpen" @close="closeModal">
        <template #header>
          <h3>Thông báo từ hệ thống</h3>
        </template>
        <div>
          Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào
          nút Close.
        </div>
      </Modal>
    </div>
    <div>
      <h1>B6</h1>
      <Card>
        <template #header> Thông tin sản phẩm </template>

        <template #default>
          Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi
          bật và giá cả hợp lý.
        </template>

        <template #footer>
          <button class="btn">Xem chi tiết</button>
        </template>
      </Card>
    </div>
    <MessageParent />
    <ListUser />
  </div>
</template>

<script setup>
import { ref } from "vue";
// import Parents from "./components/Parents.vue";
// import Header from "./components/Header.vue";
import ParentComponent from "./components/ParentComponent.vue";
import ProductParent from "./components/ProductParent.vue";
import CountParent from "./components/CountParent.vue";
import TodoApp from "./components/TodoApp.vue";
import Modal from "./components/Modal.vue";
import Card from "./components/Card.vue";
import MessageParent from "./components/MessageParent.vue";
import ListUser from "./components/ListUser.vue";

const isModalOpen = ref(false);

const openModal = () => {
  isModalOpen.value = true;
};

const closeModal = () => {
  isModalOpen.value = false;
};

// const clicking = (data) => {
//   console.log(data);
// };
</script>

<style></style>
