<template>
  <nav class="w-full z-50 absolute top-0 left-0 bg-transparent">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16 items-center">
        
        <!-- Logo -->
        <div class="flex-shrink-0 flex items-center -ml-20">
          <router-link to="/" class="text-2xl font-bold text-white">Certifyme</router-link>
        </div>

        <!-- Menu Desktop -->
        <div class="hidden md:flex md:items-center space-x-6">
          <router-link to="/" class="text-white hover:text-gray-200">Beranda</router-link>
          <router-link to="/login" class="text-white hover:text-gray-200">Login</router-link>
          <router-link to="/langganan" class="text-white hover:text-gray-200">Langganan</router-link>
          <router-link to="/verifikasi" class="text-white hover:text-gray-200">Verifikasi</router-link>
        </div>

        <!-- Button Daftar Desktop -->
        <div class="hidden md:flex">
          <router-link
            to="/register"
            class="px-4 py-2 bg-white text-[#622EFD] rounded-md hover:bg-[#E9DEFF] transition">
            Daftar
          </router-link>
        </div>

        <!-- Mobile menu button -->
        <div class="flex md:hidden">
          <button @click="isOpen = !isOpen" type="button" class="text-white hover:text-gray-200 focus:outline-none">
            <svg v-if="!isOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 8h16M4 16h16"/>
            </svg>
            <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-if="isOpen" class="md:hidden bg-black bg-opacity-70 px-2 pt-2 pb-3 space-y-1 shadow-md">
      <router-link to="/" class="block text-white hover:text-gray-200">Beranda</router-link>
      <router-link to="/login" class="block text-white hover:text-gray-200">Login</router-link>
      <router-link to="/langganan" class="block text-white hover:text-gray-200">Langganan</router-link>
      <router-link to="/verifikasi" class="block text-white hover:text-gray-200">Verifikasi</router-link>
      <router-link 
        to="/register" 
        class="block mt-2 px-4 py-2 bg-blue-600 text-white rounded-md hover:bg-blue-700 transition">
        Daftar
      </router-link>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const isOpen = ref(false)
</script>

<style scoped>

</style>
