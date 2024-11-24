<script setup lang="ts">
import { ref } from "vue";

const emit = defineEmits(["update:isVisible"]);

defineProps({
  isVisible: {
    type: Boolean,
    required: true,
  },
});

const email = ref("");
const password = ref("");

// ログイン処理
function login() {
  console.log("ログイン処理");
}

// モーダル閉じる
function closeModal() {
  emit("update:isVisible", false);
}
</script>

<template>
  <div
    @click.self="closeModal"
    v-if="isVisible"
    class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center z-50"
  >
    <div class="bg-white p-6 rounded-lg shadow-lg max-w-sm w-full">
      <h2 class="text-xl font-bold mb-8">ログイン</h2>
      <div class="mb-12">
        <div class="mb-4">
          <label for="email">メールアドレス</label>
          <input
            type="email"
            id="email"
            v-model="email"
            placeholder="example@domain.com"
            class="mt-2 block w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>
        <div class="mb-4">
          <label for="password">パスワード</label>
          <input
            type="password"
            id="password"
            v-model="password"
            placeholder="test1111"
            class="mt-2 block w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>
      </div>
      <div class="flex justify-between">
        <button @click="login" class="bg-green-600 text-white p-3 rounded-md">ログイン</button>
        <button @click="closeModal" class="bg-red-500 text-white p-3 rounded-md">閉じる</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* 必要に応じてカスタムスタイルを追加 */
</style>
