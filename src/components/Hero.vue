<script setup>
// 这里可以添加个人信息
const personalInfo = {
  name: '你的名字',
  title: '职位/职业',
  description: '简短的自我介绍，描述你的专业领域和职业目标。',
  avatar: '', // 可以添加头像链接
  social: {
    github: 'https://github.com/yourusername',
    linkedin: '',
    email: 'your.email@example.com'
  }
}
</script>

<template>
  <section id="hero" class="pt-24 pb-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-6xl mx-auto">
      <div class="text-center">
        <!-- 头像 (可选) -->
        <div v-if="personalInfo.avatar" class="mb-8">
          <img
            :src="personalInfo.avatar"
            :alt="personalInfo.name"
            class="w-32 h-32 rounded-full mx-auto object-cover border-4 border-blue-500 dark:border-blue-400"
          />
        </div>

        <!-- 名字和标题 -->
        <h1 class="text-5xl sm:text-6xl font-bold text-gray-900 dark:text-white mb-4">
          {{ personalInfo.name }}
        </h1>
        <h2 class="text-2xl sm:text-3xl text-blue-600 dark:text-blue-400 mb-6">
          {{ personalInfo.title }}
        </h2>
        <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto mb-8">
          {{ personalInfo.description }}
        </p>

        <!-- 社交链接 -->
        <div class="flex justify-center space-x-4">
          <a
            v-if="personalInfo.social.github"
            :href="personalInfo.social.github"
            target="_blank"
            class="p-3 bg-gray-900 dark:bg-gray-700 text-white rounded-lg hover:bg-gray-700 dark:hover:bg-gray-600 transition-colors"
            aria-label="GitHub"
          >
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
            </svg>
          </a>
          <a
            v-if="personalInfo.social.linkedin"
            :href="personalInfo.social.linkedin"
            target="_blank"
            class="p-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors"
            aria-label="LinkedIn"
          >
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
            </svg>
          </a>
          <a
            v-if="personalInfo.social.email"
            :href="`mailto:${personalInfo.social.email}`"
            class="p-3 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-colors"
            aria-label="Email"
          >
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
