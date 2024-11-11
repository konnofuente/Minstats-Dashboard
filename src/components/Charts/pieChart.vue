<template>
    <div class="mt-2 bg-white dark:bg-gray-800 p-0 w-full rounded-md box-border border dark:border-gray-700">
        <div class="head p-5">
            <h1 class="text-yellow-400 text-lg font-semibold">{{ title }}</h1>
            <p class="text-gray-400">{{ subtitle }}</p>
          </div>
  
      <div class="wrapper-chart mt-5">
        <apexchart
          width="100%"
          height="380"
          type="pie"
          :options="options"
          :series="series"
        ></apexchart>
        <div class="p-3"></div>
        <br />

      </div>
    </div>
  </template>
  
  <script>
  
  export default {
    name: "PieChart",

    props: {
        title: {
        type: String,
        default: "5,355",
      },
      subtitle: {
        type: String,
        default: "User signups this week",
      },
      series: {
        type: Array,
        default: () => [44, 55, 13, 43], // Example data for pie chart
      },
      options: {
        type: Object,
        default: () => ({
          chart: {
            type: "pie",
          },
          labels: ["Direct", "Referral", "Organic", "Social"],
          responsive: [
            {
              breakpoint: 480,
              options: {
                chart: {
                  width: 200,
                },
                legend: {
                  position: "bottom",
                },
              },
            },
          ],
        }),
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add any specific styles here if needed */
  </style>
  