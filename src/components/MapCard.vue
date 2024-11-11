<template>
    <div class=" h-full mt-2 bg-white dark:bg-gray-800 p-0 w-full rounded-md box-border border dark:border-gray-700">
      <!-- Header Section with Title and Subtitle -->
      <div class="head p-5">
        <h1 class="text-yellow-400 text-lg font-semibold">{{ title }}</h1>
        <p class="text-gray-400">{{ subtitle }}</p>
      </div>
  
      <!-- Map Container -->
      <div class="map-container p-5 min-h-full">
        <LMap
          :zoom="7"
          :center="[7.3697, 12.3547]"
          style="height: 380px; width: 100%; border-radius: 8px"
        >
          <LTileLayer :url="tileLayerUrl" />
        </LMap>
      </div>
    </div>
  </template>
  
  <script>
  import { LMap, LTileLayer } from "vue3-leaflet";
  import "leaflet/dist/leaflet.css";
  
  export default {
    name: "MapCard",
    components: {
      LMap,
      LTileLayer,
    },
    props: {
      title: {
        type: String,
        default: "Map of Cameroon",
      },
      subtitle: {
        type: String,
        default: "Explore geographical details of Cameroon.",
      },
    },
    data() {
      return {
        tileLayerUrl: "https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
      };
    },
  };
  </script>
  
  <style scoped>
  .map-container {
    position: relative;
    overflow: hidden;
    border-radius: 8px;
  }
  </style>
  