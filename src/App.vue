<script setup lang="ts">

import ResponsiveNavbar from './components/ResponsiveNavbar.vue'
import HeroSection from './components/HeroSection.vue'
import CookiePopup from './components/CookiePopup.vue'
import BaseModal from './components/BaseModal.vue';

import { ref } from 'vue';

const showModal = ref(false);
</script>

<template>
  <div>
    <ResponsiveNavbar />
    <HeroSection />
    <CookiePopup />
  </div>

  <div class="p-8">
    <button @click="showModal = true" class="px-4 py-2 bg-blue-500 text-white rounded-lg">
      Open Modal
    </button>
  </div>

  <BaseModal :isOpen="showModal" title="Sign Up" @close="showModal = false">
    <p>This is a reusable modal!</p>
  </BaseModal>
</template>
