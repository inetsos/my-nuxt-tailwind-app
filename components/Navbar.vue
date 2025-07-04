<template>
  <nav class="bg-white shadow sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center">
      <NuxtLink to="/" class="text-2xl font-bold text-blue-600">☕ CoffeeBoard</NuxtLink>
      <div class="space-x-4">
        <NuxtLink to="/" class="text-gray-600 hover:text-blue-600">홈</NuxtLink>
        <NuxtLink to="/order" class="text-gray-600 hover:text-blue-600">주문</NuxtLink>
        <NuxtLink to="/admin" class="text-gray-600 hover:text-blue-600">관리자</NuxtLink>
      </div>
    </div>
  </nav>
</template>