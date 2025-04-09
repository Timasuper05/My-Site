<script setup lang="ts">
import { ref } from 'vue';
import Header from './components/Header.vue';
import About from './components/About.vue';
import Skills from './components/Skills.vue';
import Contact from './components/Contact.vue';
import CodeBackground from './components/CodeBackground.vue';

const darkMode = ref(false);

const toggleDarkMode = () => {
  darkMode.value = !darkMode.value;
  document.documentElement.classList.toggle('dark');
};
</script>

<template>
  <div :class="{ 'dark': darkMode }" class="min-h-screen bg-white dark:bg-gray-900 transition-colors duration-300 relative overflow-hidden">
    <CodeBackground />
    <div class="relative z-10">
      <Header :darkMode="darkMode" @toggle-dark-mode="toggleDarkMode" />
      <main class="container mx-auto px-4 py-8">
        <About />
        <Skills />
        <Contact />
      </main>
    </div>
  </div>
</template>