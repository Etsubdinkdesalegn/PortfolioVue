<template>
  <nav class="bg-white dark:bg-gray-800 shadow-md sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
      <div class="text-2xl font-bold text-green-600 dark:text-green-400">
        <img :src="logo" alt="My Portfolio" class="w-10 h-10 rounded-full border-2 border-green-500">
      </div>
    <!-- Desktop Menu -->
      <ul class="hidden md:flex space-x-6 text-gray-700 dark:text-gray-300">
        <li><router-link to="/" class="hover:text-green-500">Home</router-link></li>
        <li><router-link to="/about" class="hover:text-green-500">About</router-link></li>
        <li><router-link to="/skills" class="hover:text-green-500">Skills</router-link></li>
        <li><router-link to="/projects" class="hover:text-green-500">Projects</router-link></li>
        <li><router-link to="/contact" class="hover:text-green-500">Contact</router-link></li>
      </ul>
       <!-- Mobile Toggle Button -->
      <button @click="toggleMenu" class="md:hidden focus:outline-none">
        <svg v-if="!menuOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>
    <!-- Mobile Menu -->
    <div v-if="menuOpen" class="md:hidden px-6 pb-4 space-y-2 text-gray-700 dark:text-gray-300">
      <router-link @click="closeMenu" to="/" class="block py-2 hover:text-green-500">Home</router-link>
      <router-link @click="closeMenu" to="/about" class="block py-2 hover:text-green-500">About</router-link>
      <router-link @click="closeMenu" to="/skills" class="block py-2 hover:text-green-500">Skills</router-link>
      <router-link @click="closeMenu" to="/projects" class="block py-2 hover:text-green-500">Projects</router-link>
      <router-link @click="closeMenu" to="/contact" class="block py-2 hover:text-green-500">Contact</router-link>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
import logo from '../assets/homepage.png';
const menuOpen = ref(false)

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}

const closeMenu = () => {
  menuOpen.value = false
}
</script>
