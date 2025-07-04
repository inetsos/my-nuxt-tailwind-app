<template>
  <div class="flex flex-col space-y-2">
    <label :for="id" class="text-sm font-medium text-gray-700">{{ label }}</label>
    <input
      :id="id"
      :type="type"
      :placeholder="placeholder"
      class="px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-blue-500"
      :value="modelValue"
      @input="$emit('update:modelValue', ($event.target as HTMLInputElement).value)"
    />
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  id: string
  label: string
  type?: string
  placeholder?: string
  modelValue: string
}>()

const emit = defineEmits(['update:modelValue'])
</script>
