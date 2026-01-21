<script setup>
const experiences = [
  {
    company: '公司名称',
    position: '职位名称',
    duration: '2023.01 - 至今',
    description: '描述你在这个职位的主要工作内容和成就',
    achievements: [
      '成就或项目 1',
      '成就或项目 2',
      '成就或项目 3'
    ]
  },
  {
    company: '上一家公司',
    position: '职位名称',
    duration: '2021.06 - 2022.12',
    description: '描述你在这个职位的主要工作内容和成就',
    achievements: [
      '成就或项目 1',
      '成就或项目 2'
    ]
  }
]
</script>

<template>
  <section id="experience" class="py-16 px-4 sm:px-6 lg:px-8 bg-white dark:bg-gray-800">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-12 text-center">
        工作经历
      </h2>

      <div class="space-y-8">
        <div
          v-for="(exp, index) in experiences"
          :key="index"
          class="border-l-4 border-blue-500 pl-6 pb-8"
        >
          <div class="flex flex-col sm:flex-row sm:justify-between sm:items-start mb-2">
            <div>
              <h3 class="text-2xl font-semibold text-gray-900 dark:text-white">
                {{ exp.position }}
              </h3>
              <p class="text-xl text-blue-600 dark:text-blue-400">
                {{ exp.company }}
              </p>
            </div>
            <span class="text-gray-600 dark:text-gray-400 mt-2 sm:mt-0">
              {{ exp.duration }}
            </span>
          </div>

          <p class="text-gray-700 dark:text-gray-300 mb-4">
            {{ exp.description }}
          </p>

          <ul class="list-disc list-inside space-y-2 text-gray-600 dark:text-gray-400">
            <li v-for="(achievement, i) in exp.achievements" :key="i">
              {{ achievement }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
