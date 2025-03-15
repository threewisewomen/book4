<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <div class="container mx-auto p-4">
    <h1 class="text-3xl font-bold text-center mb-4">{{ msg }}</h1>

    <div class="card bg-white p-4 rounded shadow mb-4">
      <button type="button" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600" @click="count++">count is {{ count }}</button>
      <p class="mt-2">
        Edit
        <code class="bg-gray-200 p-1 rounded">components/HelloWorld.vue</code> to test HMR
      </p>
    </div>

    <p class="text-center">
      Check out
      <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank" class="text-blue-500 hover:underline">create-vue</a>, the official Vue + Vite starter
    </p>
    <p class="text-center">
      Learn more about IDE Support for Vue in the
      <a href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support" target="_blank" class="text-blue-500 hover:underline">Vue Docs Scaling up Guide</a>.
    </p>
    <p class="read-the-docs text-center mt-4">Click on the Vite and Vue logos to learn more</p>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>