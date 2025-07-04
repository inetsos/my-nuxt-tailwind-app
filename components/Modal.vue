<template>
  <div
    class="fixed inset-0 bg-black/40 flex items-center justify-center z-50"
    v-if="show"
  >
    <div class="bg-white rounded shadow-lg p-6 max-w-md w-full">
      <h2 class="text-xl font-bold mb-4">{{ title }}</h2>
      <p class="mb-4 text-gray-600">
        <slot />
      </p>
      <div class="flex justify-end space-x-2">
        <button class="px-4 py-2 bg-gray-200 rounded hover:bg-gray-300" @click="onCancel">취소</button>
        <button class="px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700" @click="onConfirm">확인</button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  show: boolean
  title: string
}>()

const emit = defineEmits(['confirm', 'cancel'])

const onConfirm = () => emit('confirm')
const onCancel = () => emit('cancel')
</script>