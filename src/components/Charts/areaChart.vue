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
          type="area"
          :options="options"
          :series="series"
        ></apexchart>
        <br />

      </div>
    </div>
  </template>
  
  <script>
  import ApexCharts from "apexcharts";
//   import VueApexCharts from "vue3-apexcharts";
  
  export default {
    name: "AreaChart",
    components: {
    //   apexchart: VueApexCharts,
    },
    props: {
      title: {
        type: String,
        default: "5,355",
      },
      subtitle: {
        type: String,
        default: "Visitor this week",
      },
      percentage: {
        type: Number,
        default: 47.9,
      },
      series: {
        type: Array,
        default: () => [
          {
            name: "Visitor",
            data: [30, 40, 45, 50, 49, 60, 70, 91],
          },
          {
            name: "Visitor",
            data: [30, 50, 45, 50, 19, 50, 70, 41],
          },
        ],
      },
      options: {
        type: Object,
        default: () => ({
          chart: {
            toolbar: {
              show: false,
            },
            zoom: {
              enabled: false,
            },
            sparkline: {
              enabled: true,
            },
          },
          legend: {
            show: false,
          },
          xaxis: {
            show: false,
          },
          yaxis: {
            show: false,
          },
          colors: ["#4f46e5", "#34d399"],
          dataLabels: {
            enabled: false,
          },
          fill: {
            type: "gradient",
            gradient: {
              shadeIntensity: 0,
              opacityFrom: 0,
              opacityTo: 0.3,
              stops: [0, 90, 100],
            },
          },
          stroke: {
            curve: "smooth",
          },
          markers: {
            size: 5, // Adds points on each data value
            colors: ["#4f46e5", "#34d399"], // Marker colors for each line
            strokeColors: "#ffffff",
            strokeWidth: 2,
            hover: {
              size: 7, // Increase size on hover
            },
          },
        }),
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add any specific styles here if needed */
  </style>
  