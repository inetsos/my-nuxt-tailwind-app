<template>
  <div class="min-h-screen bg-gray-100 text-gray-800">
    <Navbar />

    <main class="px-4 pb-20 flex items-center justify-center min-h-[calc(100vh-64px)]">
      <NuxtPage />
    </main>

    <Footer class="fixed bottom-0 w-full bg-gray-200 py-4 text-center" />
  </div>
</template>

<script setup lang="ts">
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
</script>