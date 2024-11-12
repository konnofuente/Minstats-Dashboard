<!-- LineChart.vue -->
<template>
    <div class="bg-white dark:bg-gray-800 p-5 rounded-md border dark:border-gray-700">
      <div class="flex justify-between items-center mb-4">
        <h2 class="font-medium text-lg text-gray-800 dark:text-gray-200">Page Statistics</h2>
        <button class="text-gray-500 dark:text-gray-400">
          <Icon icon="mdi:menu" />
        </button>
      </div>
      <apexchart
        width="100%"
        height="300"
        type="line"
        :options="chartOptions"
        :series="seriesData"
      ></apexchart>
    </div>
  </template>
  
  <script>
  import { defineComponent } from "vue";
//   import VueApexCharts from "vue3-apexcharts";
  
  export default defineComponent({
    name:"LineChart",
    // components: {
    //   apexchart: VueApexCharts,
    // },
    props: {
      seriesData: {
        type: Array,
        required: true,
      },
    },
    computed: {
      chartOptions() {
        return {
          chart: {
            type: "line",
            toolbar: {
              show: false,
            },
          },
          stroke: {
            width: [3, 3, 3],
            dashArray: [0, 5, 8], // Controls the line style: solid, dashed, dotted
          },
          colors: ["#3b82f6", "#10b981", "#f59e0b","#d59e02"], // Blue, Green, Yellow for each series line
          xaxis: {
            type: "category",
            categories: [
              "01 Jan", "02 Jan", "03 Jan", "04 Jan", "05 Jan", "06 Jan", "07 Jan",
              "08 Jan", "09 Jan", "10 Jan", "11 Jan", "12 Jan",
            ],
            labels: {
              style: {
                colors: "#9ca3af", // Label color
              },
            },
          },
          yaxis: {
            labels: {
              style: {
                colors: "#9ca3af",
              },
            },
          },
          tooltip: {
            theme: "dark",
          },
          legend: {
            position: "bottom",
            labels: {
              colors: "#9ca3af",
            },
          },
        };
      },
    },
  });
  </script>
  
  <style scoped>
  /* Additional styling as needed */
  </style>
  