<template>
    <div class="mt-2 bg-white dark:bg-gray-800 p-0 w-full rounded-md box-border border dark:border-gray-700">
      <!-- Header with Title and Subtitle -->
      <div class="head p-5 flex justify-between items-center">
        <div>
          <h1 class="text-yellow-400 text-lg font-semibold">{{ title }}</h1>
          <p class="text-gray-400">{{ subtitle }}</p>
        </div>
        <span>
          <h2 class="text-green-500 flex items-center">
            <span class="mr-2">{{ percentage }}%</span>
            <Icon icon="akar-icons:arrow-up" />
          </h2>
        </span>
      </div>
  
      <!-- Chart -->
      <div class="wrapper-chart mt-5 pr-2 pl-2">
        <apexchart
          :type="chartType"
          :width="chartWidth"
          :height="chartHeight"
          :options="options"
          :series="series"
        ></apexchart>
      </div>
  
 
    </div>
  </template>
  
  <script>
  import { Icon } from '@iconify/vue'; // Import Icon if using Iconify
  
  export default {
    name:"VerticalBarChart",
    components: {
      Icon,
    },
    props: {
      title: {
        type: String,
        default: "First",
      },
      subtitle: {
        type: String,
        default: "Stats Summary",
      },
      percentage: {
        type: Number,
        default: 0,
      },
      chartType: {
        type: String,
        default: "bar",
      },
      options: {
        type: Object,
        required: true,
      },
      series: {
        type: Array,
        required: true,
      },
      chartWidth: {
        type: String,
        default: "100%",
      },
      chartHeight: {
        type: String,
        default: "380",
      },
    },
  };
  </script>
  
  <style scoped>
  /* Scoped styles if needed */
  </style>
  