<template>
<section class="flex flex-col items-center justify-center min-h-[70vh] bg-gradient-to-r from-green-400 to-blue-500 text-white px-4 text-center">
     <div class="text-2xl font-bold text-green-600 dark:text-green-400">
        <img :src="logo" alt="My Portfolio" class="w-50 h-50 rounded-full border-2 border-green-500">
      </div>
      <h1 class="text-3xl  mb-2">Etsubdink Desalegn Adamu</h1>
      <h2 class="text-2xl font-extrabold mb-4">Software Engineer</h2>

    <h1 class="text-5xl font-extrabold mb-4">Welcome to My Portfolio</h1>
  </section>
</template>

<script setup>
import logo from '../assets/homepage.png';
</script>