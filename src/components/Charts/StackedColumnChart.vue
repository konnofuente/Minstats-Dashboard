<template>
    <div class="mt-2 bg-white dark:bg-gray-800 p-0 w-full rounded-md box-border border dark:border-gray-700">
      <div class="head p-5">
        <h1 class="dark:text-yellow-400 text-lg font-semibold">{{ title }}</h1>
        <p class="text-gray-400">{{ subtitle }}</p>
      </div>
  
      <div class="wrapper-chart mt-5">
        <apexchart
          width="100%"
          height="380"
          type="bar"
          :options="options"
          :series="series"
        ></apexchart>
        <div class="p-3"></div>
        <br />
      </div>
    </div>
  </template>
  
  <script>
  import ApexCharts from 'vue3-apexcharts';
  
  export default {
    name: "StackedColumnChart",
    components: {
      apexchart: ApexCharts,
    },
    props: {
      title: {
        type: String,
        default: "Sales Performance",
      },
      subtitle: {
        type: String,
        default: "Monthly Sales Data by Product Category",
      },
      series: {
        type: Array,
        default: () => [
          {
            name: "Product A",
            data: [44, 55, 41, 67, 22, 43],
          },
          {
            name: "Product B",
            data: [13, 23, 20, 8, 13, 27],
          },
          {
            name: "Product C",
            data: [11, 17, 15, 15, 21, 14],
          },
          {
            name: "Product D",
            data: [21, 7, 25, 13, 22, 8],
          },
        ],
      },
      options: {
        type: Object,
        default: () => ({
          chart: {
            type: "bar",
            stacked: true,
            toolbar: {
              show: true,
            },
          },
          plotOptions: {
            bar: {
              horizontal: false,
              borderRadius: 5,
            },
          },
          xaxis: {
            categories: ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
          },
          yaxis: {
            title: {
              text: "Sales (in thousands)",
            },
          },
          fill: {
            opacity: 1,
          },
          legend: {
            position: "top",
            horizontalAlign: "left",
          },
          colors: ["#FF4560", "#00E396", "#008FFB", "#775DD0"],
        }),
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add any specific styles here if needed */
  </style>
  