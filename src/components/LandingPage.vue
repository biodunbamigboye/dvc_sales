<script setup lang="ts">
  import { ref } from 'vue'
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import { faBars, faTimes } from '@fortawesome/free-solid-svg-icons';

  const isSidebarOpen = ref(false)

  const toggleSidebar = () => {
    isSidebarOpen.value = !isSidebarOpen.value;
  }
</script>


<template>
  <div class="bg-indigo-600 min-h-screen text-white">
    <header class="fixed bg-indigo-600 top-0 z-10 w-full h-16 flex justify-between items-center">
      <div class="flex justify-between items-center w-full px-6 py-4">
        <h1 class="text-2xl font-sans italic">DVC Sales</h1>

        <button @click="toggleSidebar" class="md:hidden text-white">
          <FontAwesomeIcon :icon="faBars" size="2x" />
        </button>
        <nav class="hidden md:flex space-x-6">
          <a href="#">Home</a>
          <a href="#">Buying</a>
          <a href="#">Selling</a>
          <a href="#">Listings</a>
          <a href="#">Contact</a>
        </nav>

        <nav v-if="isSidebarOpen" :class="['fixed inset-y-0 p-4 right-0 z-30 w-56 transform transition-all duration-500 md:hidden bg-blue-700', isSidebarOpen ? 'translate-x-0' : 'translate-x-full']">
          <div class="flex justify-end" @click="toggleSidebar">
            <FontAwesomeIcon :icon="faTimes" size="2x" class="text-white hover:text-red-600" />
          </div>
          <div class="flex flex-col gap-4">
            <a href="#">Home</a>
            <a href="#">Buying</a>
            <a href="#">Selling</a>
            <a href="#">Listings</a>
            <a href="#">Contact</a>
          </div>
          
        </nav>
      </div>
      <div v-if="isSidebarOpen" @click="toggleSidebar" class="fixed inset-0 bg-black/50 z-20 md:hidden"></div>
    </header>

    <section class="flex flex-col md:flex-row items-center gap-8 justify-between px-8 md:px-14 lg:px-20 pb-14 pt-28">
      <div class="md:w-1/2 text-center md:text-left">
        <h2 class="text-2xl  font-bold italic">The Most Recommended <span class="block">DVC Resale Broker</span></h2>
        <p class="font-semibold text-lg max-w-xl mt-6">The Most Recommended DVC Resale Broker.<span class="block">We have helped over 10,000 families enjoy the magic of DVC since 1993.</span><span class="block">Take advantage of 6.9% commission NOW!</span>Lowest Commission Guaranteed. Easy to Use Online Platform. Verified Listings Updated in Real Time</p>
        <div class="flex flex-col md:flex-row gap-4 items-center mt-10">
          <router-link to="/dashboard">
            <button class="px-2 py-1 cursor-pointer border-white border text-sm rounded-sm">View DVC Resale Listings</button>
          </router-link>
          
          <button class="px-2 py-1 cursor-pointer border-white border text-sm rounded-sm bg-green-600">Sell My DVC Contract</button>
        </div>
      </div>

      <div class="md:w-1/2 relative flex justify-center">
        <div class="lg:w-1/3 w-1/2 rotate-6">
          <img src="@/assets/iphone.png" alt="" >
        </div>
        <div class="absolute w-1/3 right-0 bottom-0">
          <img src="@/assets/code.png" alt="" >
        </div>
        
      </div>
     
    </section>
  </div>
</template>