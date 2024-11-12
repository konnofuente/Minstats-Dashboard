<template>
  <div class="dashboard p-4">
    <!-- end nav -->
    <div class="mt-2 w-full">
      <div
        class="lg:flex grid-cols-1 lg:space-y-0 space-y-3 gap-5 justify-between"
      >
        <div>
          <p class="uppercase text-xs text-gray-700 font-semibold">overview</p>
          <h1 class="text-2xl text-gray-900 dark:text-gray-200 font-medium">
            Dashboard
          </h1>
        </div>
      </div>
    </div>

    <div class="grid md:flex justify-between">
      <!-- grid wrapper card -->
      <div
        class="wrapper-card bg-white dark:bg-gray-800 text-white rounded-lg p-6 md:w-[59%] w-full"
      >
        <div class="flex justify-between items-center mb-4">
          <div>
            <h1 class="dark:text-yellow-400 text-black text-lg font-semibold">
              Statistics per Service
            </h1>
            <p class="text-gray-400">Stats Summary</p>
          </div>
          <button class="bg-yellow-400 text-gray-900 px-4 py-2 rounded">
            Details
          </button>
        </div>
        <div class="grid lg:grid-cols-4 grid-cols-1 md:grid-cols-2 gap-4 mt-5">
          <IconDataCard
            title="300"
            subtitle="entry xxxxx"
            additionalInfo="+5% since last year"
            bgColor="yellow-100"
            iconBgColor="orange-200"
            iconColor="orange-600"
          >
            <template #icon>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                aria-hidden="true"
                role="img"
                width="30px"
                height="30px"
                preserveAspectRatio="xMidYMid meet"
                viewBox="0 0 32 32"
              >
                <path
                  fill="none"
                  d="M8.007 24.93A4.996 4.996 0 0 1 13 20h6a4.996 4.996 0 0 1 4.993 4.93a11.94 11.94 0 0 1-15.986 0ZM20.5 12.5A4.5 4.5 0 1 1 16 8a4.5 4.5 0 0 1 4.5 4.5Z"
                />
                <path
                  fill="currentColor"
                  d="M26.749 24.93A13.99 13.99 0 1 0 2 16a13.899 13.899 0 0 0 3.251 8.93l-.02.017c.07.084.15.156.222.239c.09.103.187.2.28.3c.28.304.568.596.87.87c.092.084.187.162.28.242c.32.276.649.538.99.782c.044.03.084.069.128.1v-.012a13.901 13.901 0 0 0 16 0v.012c.044-.031.083-.07.128-.1c.34-.245.67-.506.99-.782c.093-.08.188-.159.28-.242c.302-.275.59-.566.87-.87c.093-.1.189-.197.28-.3c.071-.083.152-.155.222-.24ZM16 8a4.5 4.5 0 1 1-4.5 4.5A4.5 4.5 0 0 1 16 8ZM8.007 24.93A4.996 4.996 0 0 1 13 20h6a4.996 4.996 0 0 1 4.993 4.93a11.94 11.94 0 0 1-15.986 0Z"
                />
              </svg>
            </template>
          </IconDataCard>
          <IconDataCard
            title="300"
            subtitle="entry xxxxx"
            additionalInfo="+5% since last year"
            bgColor="yellow-100"
            iconBgColor="orange-200"
            iconColor="orange-600"
          >
            <template #icon>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                aria-hidden="true"
                role="img"
                width="30px"
                height="30px"
                preserveAspectRatio="xMidYMid meet"
                viewBox="0 0 32 32"
              >
                <path
                  fill="none"
                  d="M8.007 24.93A4.996 4.996 0 0 1 13 20h6a4.996 4.996 0 0 1 4.993 4.93a11.94 11.94 0 0 1-15.986 0ZM20.5 12.5A4.5 4.5 0 1 1 16 8a4.5 4.5 0 0 1 4.5 4.5Z"
                />
                <path
                  fill="currentColor"
                  d="M26.749 24.93A13.99 13.99 0 1 0 2 16a13.899 13.899 0 0 0 3.251 8.93l-.02.017c.07.084.15.156.222.239c.09.103.187.2.28.3c.28.304.568.596.87.87c.092.084.187.162.28.242c.32.276.649.538.99.782c.044.03.084.069.128.1v-.012a13.901 13.901 0 0 0 16 0v.012c.044-.031.083-.07.128-.1c.34-.245.67-.506.99-.782c.093-.08.188-.159.28-.242c.302-.275.59-.566.87-.87c.093-.1.189-.197.28-.3c.071-.083.152-.155.222-.24ZM16 8a4.5 4.5 0 1 1-4.5 4.5A4.5 4.5 0 0 1 16 8ZM8.007 24.93A4.996 4.996 0 0 1 13 20h6a4.996 4.996 0 0 1 4.993 4.93a11.94 11.94 0 0 1-15.986 0Z"
                />
              </svg>
            </template>
          </IconDataCard>
          <IconDataCard
            title="300"
            subtitle="entry xxxxx"
            additionalInfo="+5% since last year"
            bgColor="yellow-100"
            iconBgColor="orange-200"
            iconColor="orange-600"
          >
            <template #icon>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                aria-hidden="true"
                role="img"
                width="30px"
                height="30px"
                preserveAspectRatio="xMidYMid meet"
                viewBox="0 0 32 32"
              >
                <path
                  fill="none"
                  d="M8.007 24.93A4.996 4.996 0 0 1 13 20h6a4.996 4.996 0 0 1 4.993 4.93a11.94 11.94 0 0 1-15.986 0ZM20.5 12.5A4.5 4.5 0 1 1 16 8a4.5 4.5 0 0 1 4.5 4.5Z"
                />
                <path
                  fill="currentColor"
                  d="M26.749 24.93A13.99 13.99 0 1 0 2 16a13.899 13.899 0 0 0 3.251 8.93l-.02.017c.07.084.15.156.222.239c.09.103.187.2.28.3c.28.304.568.596.87.87c.092.084.187.162.28.242c.32.276.649.538.99.782c.044.03.084.069.128.1v-.012a13.901 13.901 0 0 0 16 0v.012c.044-.031.083-.07.128-.1c.34-.245.67-.506.99-.782c.093-.08.188-.159.28-.242c.302-.275.59-.566.87-.87c.093-.1.189-.197.28-.3c.071-.083.152-.155.222-.24ZM16 8a4.5 4.5 0 1 1-4.5 4.5A4.5 4.5 0 0 1 16 8ZM8.007 24.93A4.996 4.996 0 0 1 13 20h6a4.996 4.996 0 0 1 4.993 4.93a11.94 11.94 0 0 1-15.986 0Z"
                />
              </svg>
            </template>
          </IconDataCard>
          <IconDataCard
            title="300"
            subtitle="entry xxxxx"
            additionalInfo="+5% since last year"
            bgColor="yellow-100"
            iconBgColor="orange-200"
            iconColor="orange-600"
          >
            <template #icon>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                aria-hidden="true"
                role="img"
                width="30px"
                height="30px"
                preserveAspectRatio="xMidYMid meet"
                viewBox="0 0 32 32"
              >
                <path
                  fill="none"
                  d="M8.007 24.93A4.996 4.996 0 0 1 13 20h6a4.996 4.996 0 0 1 4.993 4.93a11.94 11.94 0 0 1-15.986 0ZM20.5 12.5A4.5 4.5 0 1 1 16 8a4.5 4.5 0 0 1 4.5 4.5Z"
                />
                <path
                  fill="currentColor"
                  d="M26.749 24.93A13.99 13.99 0 1 0 2 16a13.899 13.899 0 0 0 3.251 8.93l-.02.017c.07.084.15.156.222.239c.09.103.187.2.28.3c.28.304.568.596.87.87c.092.084.187.162.28.242c.32.276.649.538.99.782c.044.03.084.069.128.1v-.012a13.901 13.901 0 0 0 16 0v.012c.044-.031.083-.07.128-.1c.34-.245.67-.506.99-.782c.093-.08.188-.159.28-.242c.302-.275.59-.566.87-.87c.093-.1.189-.197.28-.3c.071-.083.152-.155.222-.24ZM16 8a4.5 4.5 0 1 1-4.5 4.5A4.5 4.5 0 0 1 16 8ZM8.007 24.93A4.996 4.996 0 0 1 13 20h6a4.996 4.996 0 0 1 4.993 4.93a11.94 11.94 0 0 1-15.986 0Z"
                />
              </svg>
            </template>
          </IconDataCard>
        </div>
      </div>

      <!-- end wrapper card -->
      <div class="md:w-[40%]">
        <LineChart :seriesData="lineSeriesData" />
      </div>
    </div>

    <div class="mt-2 lg:flex block lg:gap-2">
      <VerticalBarChart
        title="First"
        subtitle="Stats Summary"
        :percentage="27.9"
        chartType="bar"
        :options="optionsBar"
        :series="seriesBar"
      />

      <AreaChart
        title="Second Statistics"
        subtitle="Second Statistics"
        :percentage="47.9"
        :series="seriesVisitor"
        :options="optionsVisitor"
      />

      <PieChart
        title="Third Data"
        subtitle="User signups this week"
        :series="seriesDonut"
        :options="optionsDonut"
      />
    </div>

    <div class="grid md:grid-cols-3 grid-col-1">
      <div
        class="col-span-2 mt-2 bg-white dark:bg-gray-800 p-5 w-full rounded-md box-border border dark:border-gray-700"
      >
        <h2 class="font-bold text-lg text-gray-800 dark:text-gray-200">
          Latest Transactions
        </h2>
        <p class="text-gray-400 font-lexend font-normal">
          This is a list of latest transactions
        </p>
        <div class="wrapping-table mt-10">
          <table
            class="w-full text-sm text-left text-gray-500 dark:text-gray-400 lg:overflow-auto overflow-x-scroll"
          >
            <thead
              class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400"
            >
              <tr>
                <th scope="col" class="uppercase px-6 py-3">#</th>
                <th scope="col" class="uppercase px-6 py-3">Transaction</th>
                <th scope="col" class="uppercase px-6 py-3">Date & Time</th>
                <th scope="col" class="uppercase px-6 py-3">Grading</th>
                <th scope="col" class="uppercase px-6 py-3">percentage</th>
              </tr>
            </thead>
            <tbody>
              <tr
                class="bg-white border-b dark:bg-gray-800 dark:border-gray-700 odd:bg-white even:bg-gray-50"
                v-for="(items, index) in tableTransaction"
                :key="items.transaction"
              >
                <td class="px-6 py-4">{{ index + 1 }}</td>
                <td class="px-6 py-4">{{ items.transaction }}</td>
                <td class="px-6 py-4">{{ items.datetime }}</td>
                <td class="px-6 py-4">
                  <div
                    class="w-full bg-gray-200 rounded-full h-4 dark:bg-gray-700"
                  >
                    <div
                      :class="{
                        'bg-green-500': items.grading >= 75,
                        'bg-yellow-500':
                          items.grading >= 50 && items.grading < 75,
                        'bg-red-500': items.grading < 50,
                      }"
                      class="h-4 rounded-full"
                      :style="{ width: items.grading + '%' }"
                    ></div>
                  </div>
                  <span
                    class="text-sm text-gray-500 dark:text-gray-400 mt-1 block"
                  >
                    {{ items.grading }}%
                  </span>
                </td>

                <td class="px-6 py-4">
                  <span
                    class="text-red-800 bg-red-300 px-3 py-1 rounded-md"
                    :class="{
                      'bg-green-400': items.grading >= 75,
                      'bg-yellow-500':
                        items.grading >= 50 && items.grading < 75,
                      'bg-red-500': items.grading < 50,
                    }"
                  >
                    {{ items.grading }}
                  </span>
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      <div class="pl-4 col-span-1">
        <MapCard
          title="Cameroon Map"
          subtitle="Cameroon regions and cities overview"
        />
      </div>

      <div>
        <StackedColumnChart
          :title="'Quarterly Revenue'"
          :subtitle="'Revenue by Product Line for Q1 2024'"
          :series="revenueData"
          :options="chartOptions"
        />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import { Icon } from "@iconify/vue";
import IconDataCard from "@/components/IconDataCard.vue";
import LineChart from "@/components/Charts/LineChart.vue";
import VerticalBarChart from "@/components/Charts/VerticalBarChart.vue";
import AreaChart from "@/components/Charts/AreaChart.vue";
import PieChart from "@/components/Charts/PieChart.vue";
import MapCard from "@/components/MapCard.vue";
import StackedColumnChart from "@/components/Charts/StackedColumnChart.vue";

export default {
  name: "Dashboard",
  data() {
    return {
      // for more guide apexchart.js
      // https://apexcharts.com/docs/chart-types/line-chart/

      // chart data area
      revenueData: [
        { name: "Product A", data: [120, 90, 70, 85] },
        { name: "Product B", data: [85, 75, 95, 100] },
      ],
      chartOptions: {
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
          categories: ["Q1", "Q2", "Q3", "Q4"],
        },
        yaxis: {
          title: {
            text: "Revenue (in thousands)",
          },
        },
        fill: {
          opacity: 1,
        },
        legend: {
          position: "bottom",
          horizontalAlign: "center",
        },
        colors: ["#FF4560", "#00E396"],
      },

      lineSeriesData: [
        {
          name: "Session Duration",
          data: [45, 60, 35, 50, 40, 20, 30, 25, 60, 30, 45, 25],
        },
        {
          name: "Page Views",
          data: [30, 50, 55, 45, 60, 40, 45, 55, 50, 65, 50, 55],
        },
        {
          name: "Total Visits",
          data: [80, 70, 90, 85, 60, 75, 70, 85, 65, 80, 75, 70],
        },
        {
          name: "Total Visits",
          data: [80, 30, 90, 85, 60, 55, 70, 84, 95, 20, 75, 30],
        },
      ],
      optionsArea: {
        xaxis: {
          categories: [2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022],
        },
        fontFamily: "Segoe UI, sans-serif",
        stroke: {
          curve: "straight",
        },
        chart: {
          toolbar: {
            show: true,
          },
          zoom: {
            enabled: false,
          },
          sparkline: {
            enabled: true,
          },
        },
        markers: {
          size: 0,
        },
        yaxis: {
          show: false,
        },
        fill: {
          type: "gradient",
          gradient: {
            shadeIntensity: 0,
            opacityFrom: 0.2,
            opacityTo: 0.5,
            stops: [0, 90, 100],
          },
        },
      },

      chart: {
        fontFamily: "lexend, sans-serif",
      },

      seriesArea: [
        {
          name: "Revenue",
          data: [30, 40, 45, 50, 49, 60, 70, 91],
        },
        {
          name: "Revenue (Previous period)",
          data: [20, 34, 45, 55, 79, 87, 90, 98],
        },
      ],

      optionsBar: {
        chart: {
          type: "bar",
          toolbar: {
            show: false, // Hide or show the toolbar
          },
        },
        xaxis: {
          categories: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul"], // Labels for x-axis
          title: {
            text: "Months", // X-axis label
            style: {
              color: "#888", // Customize label color
              fontSize: "12px",
            },
          },
          labels: {
            style: {
              colors: ["#9aa0ac"], // Customize x-axis labels color
              fontSize: "12px",
            },
          },
        },
        yaxis: {
          title: {
            text: "Values", // Y-axis label
            style: {
              color: "#888", // Customize label color
              fontSize: "12px",
            },
          },
          labels: {
            style: {
              colors: ["#9aa0ac"], // Customize y-axis labels color
              fontSize: "12px",
            },
          },
        },

        plotOptions: {
          bar: {
            horizontal: false, // Set to true for horizontal bars
            columnWidth: "50%", // Customize bar width
          },
        },
        dataLabels: {
          enabled: true, // Show data labels on bars
          style: {
            colors: ["#333"], // Data label color
          },
        },
        series: [
          {
            name: "Data Series",
            data: [30, 40, 25, 50, 49, 60, 70], // Sample data
          },
        ],
      },

      seriesBar: [
        {
          name: "Product 1",
          data: [30, 40, 45, 50, 49, 60, 70, 91],
        },
        {
          name: "Product 2",
          data: [20, 34, 45, 55, 79, 87, 90, 98],
        },
      ],
      seriesVisitor: [
        {
          name: "Visitor",
          data: [30, 40, 45, 50, 49, 60, 70, 91],
        },
        {
          name: "Visitor",
          data: [30, 50, 45, 50, 19, 50, 70, 41],
        },
      ],
      optionsVisitor: {
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
          size: 5,
          colors: ["#4f46e5", "#34d399"],
          strokeColors: "#ffffff",
          strokeWidth: 2,
          hover: {
            size: 7,
          },
        },
      },
      optionsDonut: {
        chart: {
          type: "donut",
        },
        legend: false,
        dataLabels: {
          enabled: false,
        },
        labels: ["admin", "SuperAdmin", "User", "Costumer"],
      },

      seriesDonut: [20, 15, 63, 83],
      tableTransaction: [
        {
          transaction: "Payment from Ethan Roger",
          datetime: "Apr 22, 2022",
          amount: "Rp.450.000",
          statusTransaction: "completed",
          grading: 85, // grading percentage
        },
        {
          transaction: "Payment from Taylor Neal",
          datetime: "May 2, 2022",
          amount: "Rp.250.000",
          statusTransaction: "completed",
          grading: 70,
        },
        {
          transaction: "Payment from Tobi Ferreira",
          datetime: "May 5, 2022",
          amount: "Rp.150.000",
          statusTransaction: "progress",
          grading: 50,
        },
        {
          transaction: "Payment failed from #046577",
          datetime: "May 5, 2022",
          amount: "Rp.180.000",
          statusTransaction: "cancelled",
          grading: 30,
        },
      ],
    };
    // end chart data line
  },
  components: {
    Icon,
    IconDataCard,
    LineChart,
    VerticalBarChart,
    AreaChart,
    PieChart,
    MapCard,
    StackedColumnChart,
  },
  mounted() {},
};
</script>
