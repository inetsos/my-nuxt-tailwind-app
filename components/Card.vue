<template>
  <div class="max-w-sm bg-white rounded-lg shadow-md overflow-hidden">
    <img class="w-full h-48 object-cover" :src="image" alt="카드 이미지" />
    <div class="p-4">
      <h2 class="text-xl font-bold text-gray-800">{{ title }}</h2>
      <p class="mt-2 text-gray-600 text-sm">
        <slot name="description" />
      </p>
      <div class="mt-4">
        <slot name="action" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  image: string
  title: string
}>()
</script>