<!-- IconDataCard.vue -->
<template>
    <div :class="`bg-${bgColor} w-full rounded-md p-5 border dark:border-gray-700 grid justify-start `">
      <div class="p-2 max-w-sm">
        <div :class="`bg-${iconBgColor} rounded-full w-14 h-14 text-lg p-3 `" :style="{ color: iconColor }">
          <slot name="icon"></slot>
        </div>
      </div>
      <div class="block p-2 w-full">
        <p class="font-semibold text-gray-900 dark:text-gray-200 text-xl">{{ title }}</p>
        <h2 class="font-normal text-gray-400 text-md mt-1">{{ subtitle }}</h2>
        <p class="text-blue-500 text-sm mt-1">{{ additionalInfo }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "IconDataCard",
    props: {
      title: String,
      subtitle: String,
      additionalInfo: String,
      bgColor: {
        type: String,
        default: "white",
      },
      iconBgColor: {
        type: String,
        default: "gray-200",
      },
      iconColor: {
        type: String,
        default: "black",
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add any component-specific styling here if needed */
  </style>
  