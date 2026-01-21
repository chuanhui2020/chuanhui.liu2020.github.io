<script setup>
const skillCategories = [
  {
    category: '前端开发',
    skills: [
      { name: 'Vue.js', level: 90 },
      { name: 'React', level: 85 },
      { name: 'TypeScript', level: 80 },
      { name: 'Tailwind CSS', level: 85 }
    ]
  },
  {
    category: '后端开发',
    skills: [
      { name: 'Node.js', level: 80 },
      { name: 'Python', level: 75 },
      { name: 'SQL', level: 70 }
    ]
  },
  {
    category: '工具 & 其他',
    skills: [
      { name: 'Git', level: 85 },
      { name: 'Docker', level: 70 },
      { name: 'CI/CD', level: 65 }
    ]
  }
]
</script>

<template>
  <section id="skills" class="py-16 px-4 sm:px-6 lg:px-8 bg-white dark:bg-gray-800">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-12 text-center">
        技能专长
      </h2>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(category, index) in skillCategories"
          :key="index"
          class="space-y-4"
        >
          <h3 class="text-2xl font-semibold text-gray-900 dark:text-white mb-4">
            {{ category.category }}
          </h3>

          <div
            v-for="(skill, i) in category.skills"
            :key="i"
            class="space-y-2"
          >
            <div class="flex justify-between items-center">
              <span class="text-gray-700 dark:text-gray-300">{{ skill.name }}</span>
              <span class="text-sm text-gray-500 dark:text-gray-400">{{ skill.level }}%</span>
            </div>
            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2">
              <div
                class="bg-blue-600 dark:bg-blue-400 h-2 rounded-full transition-all duration-500"
                :style="{ width: skill.level + '%' }"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
