<script setup lang="ts">
const contact = {
  email: 'timasuper05@yandex.ru',
  github: 'https://github.com/Timasuper05',
  telegram: 'https://t.me/magma1sa',
  linkedin: 'https://linkedin.com/in/your-profile'
};
</script>

<template>
  <section class="py-16 bg-gray-50 dark:bg-gray-800">
    <div class="max-w-3xl mx-auto text-center">
      <h2 class="text-3xl font-bold text-gray-800 dark:text-white mb-8">Контакты</h2>
      <div class="space-y-4">
        <a
          :href="'mailto:' + contact.email"
          class="block text-blue-600 dark:text-blue-400 hover:text-blue-700 dark:hover:text-blue-300"
        >
          {{ contact.email }}
        </a>
        <div class="flex justify-center space-x-6">
          <a
            :href="contact.github"
            target="_blank"
            class="text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
          >
            GitHub
          </a>
          <a
            :href="contact.telegram"
            target="_blank"
            class="text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
          >
            Telegram
          </a>
        
        </div>
      </div>
    </div>
  </section>
</template>