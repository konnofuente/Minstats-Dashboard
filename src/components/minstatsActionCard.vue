<template>
    <div class="bg-indigo-600 text-center p-6 rounded-lg shadow-md w-64">
      <!-- Logo/Icon Placeholder -->
      <div class="bg-white rounded-full mx-auto w-12 h-12 flex items-center justify-center mb-4">
        <Icon icon="mdi:chart-pie" class="text-indigo-600 text-2xl" />
      </div>
  
      <!-- Title -->
      <h2 class="text-white font-semibold text-[40px] mb-2">MinStats</h2>
  
      <!-- Description -->
      <p class="text-indigo-200 text-sm mb-4">
        All statistics ready with just a click
      </p>
  
      <!-- Button -->
      <button
        class="bg-white text-indigo-600 font-medium py-2 px-4 rounded-md hover:bg-indigo-100 transition duration-200"
      >
        Take Action
      </button>
    </div>
  </template>
  
  <script>
  import { Icon } from '@iconify/vue'; // Optional, if you’re using iconify for icons
  
  export default { 
    name:"MinstatsActionComponents",
    components: {
      Icon,
    },
  };
  </script>
  
  <style scoped>
  /* Scoped styles if needed */
  </style>
  