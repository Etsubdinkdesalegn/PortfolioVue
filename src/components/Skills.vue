<template>
  <section class="max-w-6xl mx-auto px-6 py-12 bg-gray-50 dark:bg-gray-900 rounded-lg">
    <h2 class="text-4xl font-bold mb-10 text-center text-gray-900 dark:text-white">Skills</h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <div v-for="(skill, index) in skills" :key="index" class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow">
        <h3 class="text-xl font-semibold mb-4 text-green-600 dark:text-green-400">{{ skill.category }}</h3>
        <ul class="list-disc list-inside space-y-1 text-gray-700 dark:text-gray-300">
          <li v-for="(item, idx) in skill.items" :key="idx">{{ item }}</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script setup>
const skills = [
  {
    category: 'Languages',
    items: ['Python', 'JavaScript ', 'Java', 'C++', 'C#', 'Dart', 'SQL']
  },
  {
    category: 'Frontend Frameworks',
    items: ['Vue.js', 'React.js']
  },
  {
    category: 'Backend Frameworks',
    items: ['Node.js', 'Django']
  },
  {
    category: 'Fullstack Frameworks',
    items: ['Laravel']
  },
  {
    category: 'Mobile Development',
    items: ['Flutter']
  },
  {
    category: 'Databases',
    items: [ 'MySQL', 'SQLite', 'MongoDB']
  },
  {
    category: 'Tools & Platforms',
    items: ['Git & GitHub', 'Docker']
  },
  {
    category: 'Testing',
    items: ['Jest', 'unit testing','Integration Testing']
  },
  {
    category: 'Design & Styling',
    items: ['Tailwind CSS', 'Bootstrap']
  },
  {
    category: 'IDEs & Editors',
    items: ['VS Code', 'PyCharm', 'IntelliJ', 'DevC++', 'Arduino IDE']
  }
]

</script>
