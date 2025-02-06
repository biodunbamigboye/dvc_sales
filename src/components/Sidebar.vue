<template>
  <div>
    <div v-if="isOpen" @click="$emit('toggle')" class="fixed inset-0 bg-black/50 lg:hidden z-30 transition-opacity" aria-hidden="true"></div>
  </div>
  <div :class="['fixed inset-y-0  left-0 z-50 shadow-lg bg-white w-64 h-screen lg:translate-x-0 border-r border-gray-300 overflow-auto transform transition-transform duration-300 ease-in-out', isOpen ? 'translate-x-0' : '-translate-x-full']">
    <div class="lg:hidden flex justify-end">
      <button @click="emit('toggle')">
        <FontAwesomeIcon :icon="faTimes"  size="2x"/>
      </button>
    </div>
    <div class="p-4">
      <h2 class="text-xl font-semibold text-indigo-500">DVC Sales</h2>
      <div class="border-b pb-2 border-gray-500">
        <p class="p-2">Dashboards</p>
        <div class="text-white p-2 flex items-center rounded justify-between bg-indigo-500">
          <p class="">Profile</p>
          <span class="bg-red-600 px-2 border rounded">2</span>
        </div>
        <div class="p-2 flex items-center justify-between">
          <p class="">I understand the rules</p>
          <span class="bg-red-600 px-2 border rounded text-white">2</span>
        </div>
        <p class="p-2">My Goal is to Sell</p>
        <div class="p-2 flex items-center justify-between">
          <p class="">Required Page</p>
          <span class="bg-red-600 px-2 border rounded text-white">8</span>
        </div>
        <div class="p-2 flex items-center justify-between">
          <p class="">Inventory For Sale</p>
          <span class=" px-2 border rounded border-gray-500">1</span>
        </div>
        <p class="p-2">Add Inventory to Sell</p>
        <p class="p-2">Active Offers</p>
        <p class="p-2">Active Agreements</p>
        <p class="p-2">Inventory Not For Sale</p>
        
      </div>
      <div class="flex flex-col gap-2.5 pt-4">
        <h3 class="text-lg font-semibold underline italic">Best Practices</h3>
        <p>Setting Your Asking Price</p>
        <p>Pending Reservations</p>
        <p>Deed Status</p>
        <p>Dealing with Low Offers</p>
        <p>Understanding 'Net to Seller'</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
  import { ref } from 'vue'
  defineProps<{ isOpen: boolean }>();
  const emit = defineEmits(["toggle"]);

  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import { faTimes } from '@fortawesome/free-solid-svg-icons';
</script>