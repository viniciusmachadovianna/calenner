<template>
  <div class="p-4 max-w-xl mx-auto">
    <h2 class="text-2xl font-bold mb-4">
      {{ currentDate.format('dddd, MMMM D, YYYY') }}
    </h2>

    <div class="space-y-2">
      <div
        v-for="hour in hours"
        :key="hour"
        class="flex items-start gap-2 border p-2 rounded-md"
      >
        <div class="w-20 text-right text-sm font-medium text-gray-600">
          {{ hour }}:00
        </div>
        <input
          v-model="tasks[hour]"
          type="text"
          class="flex-1 border rounded px-2 py-1"
          placeholder="Add a task..."
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import dayjs from 'dayjs'
import 'dayjs/locale/pt-br'
dayjs.locale('pt-br')

import { reactive } from 'vue'

const currentDate = dayjs()
const hours = Array.from({ length: 13 }, (_, i) => i + 8) // 8:00 - 20:00

const tasks = reactive({})
</script>

<style scoped>
input:focus {
  outline: none;
  border-color: #2563eb;
  box-shadow: 0 0 0 2px rgba(37, 99, 235, 0.3);
}
</style>
