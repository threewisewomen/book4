<template>
  <div class="p-6 bg-white shadow-lg rounded-md text-center">
    <h2 class="text-lg font-bold mb-4">Polygon & Multiplication Table</h2>

    <!-- Dropdowns for selecting numbers -->
    <div class="flex justify-center gap-4">
      <select v-model="num1" class="border p-2 rounded">
        <option v-for="n in 10" :key="n" :value="n">{{ n }}</option>
      </select>
      <select v-model="num2" class="border p-2 rounded">
        <option v-for="n in 10" :key="n" :value="n">{{ n }}</option>
      </select>
    </div>

    <!-- Show calculated values -->
    <p class="mt-4 text-gray-700">
      Selected Tens: <strong>{{ tens1 }}</strong> & <strong>{{ tens2 }}</strong>
    </p>
    <p class="text-gray-900 font-bold text-lg">
      {{ tens1 }} × {{ tens2 }} = {{ product }}
    </p>

    <!-- Input for 'n' range -->
    <div class="mt-4">
      <label for="nValue" class="block font-semibold">Enter Range (n):</label>
      <input
        id="nValue"
        type="number"
        v-model="n"
        class="border p-2 rounded w-20 text-center"
      />
    </div>

    <!-- Display multiplication table -->
    <div class="mt-4">
      <h3 class="text-md font-semibold mb-2">Multiplication Table</h3>
      <table class="w-full border-collapse border border-gray-300">
        <thead>
          <tr class="bg-gray-200">
            <th class="border px-2 py-1">X</th>
            <th class="border px-2 py-1">Y</th>
            <th class="border px-2 py-1">Product</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="i in n" :key="i">
            <td class="border px-2 py-1">{{ tens1 + i }}</td>
            <td class="border px-2 py-1">{{ tens2 + i }}</td>
            <td class="border px-2 py-1 font-semibold">
              {{ (tens1 + i) * (tens2 + i) }}
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";

const num1 = ref(3);
const num2 = ref(4);
const n = ref(10); // Default n value

// Convert numbers to tens
const tens1 = computed(() => num1.value * 10);
const tens2 = computed(() => num2.value * 10);
const product = computed(() => tens1.value * tens2.value);
</script>

<style scoped>
table {
  text-align: center;
}
</style>
