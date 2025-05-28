<template>
  <div class="min-h-screen bg-gray-50 p-6">
    <ProgressBar/>
    <DayView />
  </div>
</template>

<script setup>
import DayView from './components/DayView.vue'
import ProgressBar from './components/ProgressBar.vue'
</script>

<style>
body {
  font-family: system-ui, sans-serif;
  margin:0;
  width:100%;
  height: 100dvh;
  position: relative;
}
</style>
