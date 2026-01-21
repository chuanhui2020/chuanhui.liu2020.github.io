<script setup>
const contactInfo = {
  email: 'your.email@example.com',
  location: '城市, 国家',
  available: true
}
</script>

<template>
  <section id="contact" class="py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-12 text-center">
        联系方式
      </h2>

      <div class="max-w-2xl mx-auto">
        <div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-8 border border-gray-200 dark:border-gray-700">
          <div class="space-y-6">
            <div class="flex items-center space-x-4">
              <svg class="w-6 h-6 text-blue-600 dark:text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
              <div>
                <p class="text-sm text-gray-600 dark:text-gray-400">邮箱</p>
                <a :href="`mailto:${contactInfo.email}`" class="text-gray-900 dark:text-white hover:text-blue-600 dark:hover:text-blue-400">
                  {{ contactInfo.email }}
                </a>
              </div>
            </div>

            <div class="flex items-center space-x-4">
              <svg class="w-6 h-6 text-blue-600 dark:text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
              </svg>
              <div>
                <p class="text-sm text-gray-600 dark:text-gray-400">位置</p>
                <p class="text-gray-900 dark:text-white">{{ contactInfo.location }}</p>
              </div>
            </div>

            <div v-if="contactInfo.available" class="flex items-center space-x-4">
              <svg class="w-6 h-6 text-green-600 dark:text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <div>
                <p class="text-sm text-gray-600 dark:text-gray-400">状态</p>
                <p class="text-green-600 dark:text-green-400 font-semibold">开放工作机会</p>
              </div>
            </div>
          </div>

          <div class="mt-8 text-center">
            <a
              :href="`mailto:${contactInfo.email}`"
              class="inline-block px-8 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors font-semibold"
            >
              发送邮件
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
