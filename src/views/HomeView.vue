<script setup lang="ts"></script>

<template>
  <div class="flex h-screen">
    <!-- 左カラム -->
    <aside class="w-1/5 bg-blue-300 p-6">
      <h2 class="text-xl mb-4">左サイドバー</h2>
      <p>サイドバーのコンテンツです。</p>
    </aside>
    <!-- 中央カラム -->
    <main class="flex-1 bg-blue-200 p-6">
      <h2 class="text-xl mb-4">メインコンテンツ</h2>
      <p>メインコンテンツのエリアです。ここに記事や情報を表示します。</p>
    </main>
    <!-- 右カラム -->
    <aside class="w-1/5 bg-blue-300 p-6">
      <h2 class="text-xl mb-4">右サイドバー</h2>
      <p>右側のサイドバーコンテンツです。</p>
    </aside>
  </div>
</template>

<style scoped></style>
