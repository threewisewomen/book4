<template>
  <div class="min-h-screen bg-gray-100 text-gray-900">
    <header class="p-4 bg-blue-500 text-white text-center text-xl">
      Math Visualizer
    </header>
    <main class="p-6">
      <h2 class="text-lg font-bold">Welcome to Book4</h2>
      <p class="text-gray-700">Choose a math visualization below.</p>
      <!-- Placeholder for your first component -->
      <ExampleVisualization />
    </main>
  </div>
</template>

<script setup>
import ExampleVisualization from './components/ExampleVisualization.vue';
</script>

<style scoped>
</style>
