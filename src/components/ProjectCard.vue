<template>
  <section class="max-w-6xl mx-auto px-6 py-12 bg-gray-50 dark:bg-gray-900 rounded-lg">
    <h2 class="text-4xl font-bold mb-10 text-center text-gray-900 dark:text-white">My Projects</h2>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div v-for="project in projects" :key="project.id" class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow">
        <h3 class="text-xl font-semibold mb-4 text-green-600 dark:text-green-400">{{ project.title }}</h3>

        <img :src="project.image" :alt="project.title" class="w-auto h-50 object-cover rounded mb-4" />

        <p class="text-gray-700 dark:text-gray-300 mb-2">{{ project.description }}</p>

        <p class="text-gray-700 dark:text-gray-300 mb-2">
          <span class="font-semibold text-green-600 dark:text-green-400">Outcome:</span>
          <span v-html="project.outcome"></span>
        </p>

        <p class="text-gray-700 dark:text-gray-300">
          <span class="font-semibold text-green-600 dark:text-green-400">Link:</span>
          <a :href="project.link" target="_blank" class="text-blue-500 hover:underline"> {{ project.link }} </a>
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    id: 1,
    title: '1. ATMMachine C',
    image: '/src/assets/atmmachine in c.png',
    description:
      'C89, procedural programming with Account struct and ATMMachine functions using a fixed-size array for data storage; includes a menu-driven user interface.',
    outcome:
      '90% card insertion success, 85% PIN authentication success, 100% balance check success, 80% deposit success, 75% withdrawal success, 100% eject card success; 88% overall reliability based on 100 test transactions (50 valid, 50 invalid).',
    link: 'https://github.com/Etsubdinkdesalegn/ATMMachineC'
  },
  {
    id: 2,
    title: '2. ATMMachine C++',
    image: '/src/assets/atmmachine in c++.png',
    description:
      'C++98, object-oriented programming with AccountDatabase, CardReader, CashDispenser, and ATMMachine (Facade) classes using std::map for efficient data storage; features a menu-driven user interface.',
    outcome:
      '95% card insertion success, 90% PIN authentication success, 100% balance check success, 85% deposit success, 80% withdrawal success, 100% eject card success; 91% overall reliability based on 100 test transactions (50 valid, 50 invalid).',
    link: 'https://github.com/Etsubdinkdesalegn/ATMMachineCplusplus'
  },
  {
    id: 3,
    title: '3. BMI Calculator',
    image: '/src/assets/bmi calculator.png',
    description:
      'A Flutter-based BMI Calculator app lets users input gender, height, weight, and age to calculate their BMI, categorize it (Underweight, Normal, Overweight), and view health advice. It features a clean UI with sliders, buttons, and reusable widgets, styled consistently via constants.dart.',
    outcome: `Flutter & Dart (40%): Shows cross-platform app dev skills.<br>
              UI/UX Design (30%): Highlights user-friendly interface.<br>
              Modular Code (20%): Demonstrates clean, reusable code.<br>
              Logic (10%): Reflects accurate BMI calculations.<br>`,
    link: 'https://github.com/Etsubdinkdesalegn/BMICalculatorBest.git'
  },
  {
  id: 4,
  title: '4. TodoList React',
  image: '/src/assets/todolistReact.png',
  description:
    'A React-based Todo List application with login and task management pages. It uses React.js with functional components and useState hooks for state management, and CSS Modules for scoped styling. Users can add, update, delete, and manage task status with an intuitive UI.',
  outcome: `React Functionality (40%): Fully functional task tracking system.<br>
            State Management (30%): Efficient use of useState for interactivity.<br>
            Styling (20%): Clean, modular UI using CSS Modules.<br>
            CRUD Operations (10%): Create, read, update, delete tasks with modals.<br>`,
  link: 'https://github.com/Etsubdinkdesalegn/Todolist'
},
{
  id: 5,
  title: '5. Portfolio Website',
  image: '/src/assets/portfolio.png', // make sure this image exists
  description:
    'A responsive personal portfolio website built using Vue 3, Vue Router, and Tailwind CSS. It includes key sections like Home, About, Projects, Skills, and Contact. The site uses modern UI practices and component-based structure for clean maintainability.',
  outcome: `Vue 3 (40%): Demonstrates advanced SPA routing and component use.<br>
            Tailwind CSS (30%): Shows responsive and utility-first styling.<br>
            Project Structure (20%): Clean, reusable folder/component organization.<br>
            Deployment (10%): Ready for production with routing and image handling.<br>`,
  link: 'https://github.com/Etsubdinkdesalegn/PortfolioVue.git'
},{
  id: 6,
  title: '6. Portfolio Website (React.js)',
  image: '/src/assets/portfolio1.png', // Add this image in your assets
  description:
    'A personal portfolio website built using React.js and CSS Modules. It includes key sections like Home, About, Skills, Projects, and Contact, with reusable components and modular styles. It features a responsive layout and smooth navigation.',
  outcome: `React.js (40%): Showcases component-based frontend development.<br>
            CSS Modules (30%): Demonstrates clean, scoped styling practices.<br>
            UI Design (20%): Responsive and modern layout with good UX.<br>
            GitHub Deployment (10%): Hosted and managed via GitHub Pages.<br>`,
  link: 'https://github.com/Etsubdinkdesalegn/PortifolioReact.git'
}
 
];
</script>
