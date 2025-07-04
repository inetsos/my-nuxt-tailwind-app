<template>
  <div
    class="flex items-center bg-yellow-100 border-l-4 border-yellow-500 text-yellow-700 p-4"
    role="alert"
  >
    <svg class="w-5 h-5 mr-2" fill="currentColor" viewBox="0 0 20 20">
      <path
        fill-rule="evenodd"
        d="M10 18a8 8 0 100-16 8 8 0 000 16zm-.75-4h1.5v-1.5h-1.5V14zm0-6h1.5v4h-1.5V8z"
        clip-rule="evenodd"
      />
    </svg>
    <p><slot>주의 메시지입니다.</slot></p>
  </div>
</template>