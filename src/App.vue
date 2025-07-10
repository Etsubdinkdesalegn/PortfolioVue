<script setup>
import Footer from './components/Footer.vue';
import Navigation from './components/Navigation.vue'
</script>

<template>
<Navigation />
 <main class="max-w-7xl mx-auto px-4 py-8">
      <router-view />
    </main>
<Footer />
</template>

