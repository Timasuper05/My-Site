<script setup lang="ts">
const profile = {
  name: 'Тимур',
  title: 'C# ASP.NET Core Developer',
  description: `Разработчик C# и ASP.NET Core с сильными знаниями основ программирования и веб-разработки. 
  Специализируюсь на создании эффективных и масштабируемых веб-приложений с использованием современных технологий Microsoft.`
};
</script>

<template>
  <section class="py-16">
    <div class="max-w-3xl mx-auto text-center">
      <h2 class="text-4xl font-bold text-gray-800 dark:text-white mb-4">{{ profile.name }}</h2>
      <h3 class="text-2xl text-gray-600 dark:text-gray-300 mb-6">{{ profile.title }}</h3>
      <p class="text-lg text-gray-600 dark:text-gray-400 leading-relaxed">
        {{ profile.description }}
      </p>
    </div>
  </section>
</template>