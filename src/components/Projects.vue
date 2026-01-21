<script setup>
const projects = [
  {
    title: '项目名称 1',
    description: '项目的简短描述，说明项目的目标和你的贡献',
    tech: ['Vue.js', 'TypeScript', 'Tailwind CSS'],
    link: '',
    github: ''
  },
  {
    title: '项目名称 2',
    description: '项目的简短描述，说明项目的目标和你的贡献',
    tech: ['React', 'Node.js', 'MongoDB'],
    link: '',
    github: ''
  },
  {
    title: '项目名称 3',
    description: '项目的简短描述，说明项目的目标和你的贡献',
    tech: ['Python', 'Django', 'PostgreSQL'],
    link: '',
    github: ''
  }
]
</script>

<template>
  <section id="projects" class="py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-12 text-center">
        项目展示
      </h2>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6 hover:shadow-xl transition-shadow border border-gray-200 dark:border-gray-700"
        >
          <h3 class="text-2xl font-semibold text-gray-900 dark:text-white mb-3">
            {{ project.title }}
          </h3>

          <p class="text-gray-600 dark:text-gray-300 mb-4">
            {{ project.description }}
          </p>

          <div class="flex flex-wrap gap-2 mb-4">
            <span
              v-for="(tech, i) in project.tech"
              :key="i"
              class="px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-200 rounded-full text-sm"
            >
              {{ tech }}
            </span>
          </div>

          <div class="flex space-x-4">
            <a
              v-if="project.link"
              :href="project.link"
              target="_blank"
              class="text-blue-600 dark:text-blue-400 hover:underline"
            >
              查看项目 →
            </a>
            <a
              v-if="project.github"
              :href="project.github"
              target="_blank"
              class="text-gray-700 dark:text-gray-300 hover:underline"
            >
              GitHub →
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
