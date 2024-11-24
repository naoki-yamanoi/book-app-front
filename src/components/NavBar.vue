<script setup lang="ts">
import { ref } from "vue";
import LoginModal from "@/components/LoginModal.vue";

const isModalVisible = ref(false);

function openModal() {
  isModalVisible.value = true;
}
</script>

<template>
  <nav class="flex justify-between bg-blue-900 text-white p-6 w-full top-0 left-0 z-10">
    <RouterLink to="/">
      <h1 class="text-lg">Book App</h1>
    </RouterLink>
    <div @click="openModal">
      <button type="button">ログイン</button>
    </div>
  </nav>
  <!-- モーダルコンポーネント -->
  <LoginModal :isVisible="isModalVisible" @update:isVisible="isModalVisible = $event" />
</template>
