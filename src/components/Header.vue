<script setup lang="ts">
defineProps<{
  darkMode: boolean;
}>();

defineEmits<{
  (e: 'toggle-dark-mode'): void;
}>();
</script>

<template>
  <header class="bg-white dark:bg-gray-800 shadow-lg">
    <nav class="container mx-auto px-4 py-4 flex justify-between items-center">
      <h1 class="text-2xl font-bold text-gray-800 dark:text-white">Quality</h1>
      <div class="flex items-center space-x-4">
        <button
          @click="$emit('toggle-dark-mode')"
          class="p-2 rounded-lg bg-gray-200 dark:bg-gray-700"
        >
          {{ darkMode ? '🌞' : '🌙' }}
        </button>
      </div>
    </nav>
  </header>
</template>