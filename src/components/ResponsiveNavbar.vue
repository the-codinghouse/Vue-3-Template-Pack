<template>
    <nav class="bg-gray-800 text-white p-4">
      <div class="container mx-auto flex justify-between items-center">
        <!-- Logo or Brand Name -->
        <div class="text-lg font-bold">MyBrand</div>
  
        <!-- Desktop Navbar Links -->
        <div class="hidden md:flex space-x-8">
          <a href="#" class="hover:text-blue-400">Home</a>
          <a href="#" class="hover:text-blue-400">About</a>
          <a href="#" class="hover:text-blue-400">Services</a>
          <a href="#" class="hover:text-blue-400">Contact</a>
        </div>
  
        <!-- Mobile Hamburger Menu -->
        <div class="md:hidden flex items-center">
          <button @click="toggleMenu" class="text-white">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
      </div>
  
      <!-- Mobile Navbar Links -->
      <div v-if="isMenuOpen" class="md:hidden bg-gray-700 text-white p-4">
        <a href="#" class="block py-2">Home</a>
        <a href="#" class="block py-2">About</a>
        <a href="#" class="block py-2">Services</a>
        <a href="#" class="block py-2">Contact</a>
      </div>
    </nav>
  </template>
  
  <script setup lang="ts">
  import { ref } from 'vue';
  
  const isMenuOpen = ref(false);
  
  const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
  };
  </script>
  
  <style scoped>
  /* Add any additional styling if needed */
  </style>
  