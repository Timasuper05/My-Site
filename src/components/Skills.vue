<script setup lang="ts">
const skills = [
  {
    category: 'Backend Development',
    items: [
      { name: 'C#', level: 90 },
      { name: 'ASP.NET Core', level: 85 },
      { name: 'Entity Framework Core', level: 80 },
      { name: 'RESTful APIs', level: 85 }
    ]
  },
  {
    category: 'Databases',
    items: [
      { name: 'MS SQL Server', level: 80 },
      { name: 'Entity Framework', level: 75 }
    ]
  },
  {
    category: 'Tools & Others',
    items: [
      { name: 'Git', level: 75 },
      { name: 'Visual Studio', level: 85 },
      { name: 'Azure DevOps', level: 70 }
    ]
  }
];
</script>

<template>
  <section class="py-16">
    <h2 class="text-3xl font-bold text-center text-gray-800 dark:text-white mb-12">Навыки</h2>
    <div class="max-w-4xl mx-auto grid gap-8">
      <div v-for="(category, index) in skills" :key="index" class="bg-gray-50 dark:bg-gray-800 rounded-lg p-6">
        <h3 class="text-xl font-semibold text-gray-800 dark:text-white mb-4">{{ category.category }}</h3>
        <div class="space-y-4">
          <div v-for="skill in category.items" :key="skill.name" class="relative">
            <div class="flex justify-between mb-1">
              <span class="text-gray-700 dark:text-gray-300">{{ skill.name }}</span>
              <span class="text-gray-600 dark:text-gray-400">{{ skill.level }}%</span>
            </div>
            <div class="h-2 bg-gray-200 dark:bg-gray-700 rounded">
              <div
                class="h-2 bg-blue-600 rounded"
                :style="{ width: `${skill.level}%` }"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>