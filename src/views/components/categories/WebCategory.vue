<template>
  <div class="container mx-auto w-[90%] bg-gray-900 text-white">
    <div class="flex justify-between">
      <div>
        <h1 class="text-2xl font-semibold mb-2">Web Development Category</h1>
        <p class="mb-4 text-gray-400">
          You can also invert the colors—with light text on dark backgrounds.
        </p>
      </div>

      <!-- Add Category Dimension Button -->
      <button
        @click="showModal = true"
        class="bg-blue-500 hover:bg-blue-600 text-white py-2 px-4 rounded-md"
      >
        Add Category Dimension
      </button>
    </div>

    <!-- Table -->
    <table class="table-auto w-full mt-4 text-gray-300">
      <thead>
        <tr class="border-b border-gray-700">
          <th class="px-4 py-2">Name</th>
          <th class="px-4 py-2">Types</th>
          <th class="px-4 py-2">Asset</th>
          <th class="px-4 py-2">Company</th>
          <th class="px-4 py-2">Location</th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="(item, index) in items"
          :key="index"
          class="border-b border-gray-800"
        >
          <td class="px-4 py-2">{{ item.name }}</td>
          <td class="px-4 py-2">{{ item.type }}</td>
          <td class="px-4 py-2">{{ item.asset }}</td>
          <td class="px-4 py-2">{{ item.company }}</td>
          <td class="px-4 py-2">{{ item.location }}</td>
        </tr>
      </tbody>
    </table>

    <!-- Modal Form -->
    <div
      v-if="showModal"
      class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center"
    >
      <div class="bg-white text-black p-6 rounded-md w-full max-w-md">
        <h2 class="text-lg font-bold mb-4">Add Category Dimension</h2>

        <form @submit.prevent="handleFormSubmit">
          <div class="mb-4">
            <label class="block text-sm font-medium">Name</label>
            <input
              v-model="formData.name"
              type="text"
              class="w-full p-2 border border-gray-300 rounded-md"
              required
            />
          </div>

          <div class="mb-4">
            <label class="block text-sm font-medium">Type</label>
            <input
              v-model="formData.type"
              type="text"
              class="w-full p-2 border border-gray-300 rounded-md"
              required
            />
          </div>

          <div class="mb-4">
            <label class="block text-sm font-medium">Asset</label>
            <input
              v-model="formData.asset"
              type="number"
              class="w-full p-2 border border-gray-300 rounded-md"
              required
            />
          </div>

          <div class="mb-4">
            <label class="block text-sm font-medium">Company</label>
            <input
              v-model="formData.company"
              type="text"
              class="w-full p-2 border border-gray-300 rounded-md"
              required
            />
          </div>

          <div class="mb-4">
            <label class="block text-sm font-medium">Location</label>
            <input
              v-model="formData.location"
              type="text"
              class="w-full p-2 border border-gray-300 rounded-md"
              required
            />
          </div>

          <div class="flex justify-end space-x-2">
            <button
              type="button"
              @click="showModal = false"
              class="bg-gray-300 hover:bg-gray-400 py-2 px-4 rounded-md"
            >
              Cancel
            </button>
            <button
              type="submit"
              class="bg-blue-500 hover:bg-blue-600 text-white py-2 px-4 rounded-md"
            >
              Submit
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Sample data for the table
      items: [
        {
          name: "Parsley Montana",
          type: "Candy",
          asset: 7634825,
          company: "Blue Riband",
          location: "California",
        },
        {
          name: "Jarvis Pepperspray",
          type: "Treenut",
          asset: 8421678,
          company: "Burton's Maryland Specials",
          location: "Massachusetts",
        },
        {
          name: "Phillip Anthropy",
          type: "Sweetener",
          asset: 8462150,
          company: "Quaker Instant Oatmeal",
          location: "Illinois",
        },
        {
          name: "Alan Fresco",
          type: "Dairy",
          asset: 8741632,
          company: "Disney Pixar Milk Chocolate Crispy Bars",
          location: "Michigan",
        },
      ],

      // Modal control and form data
      showModal: false,
      formData: {
        name: "",
        type: "",
        asset: null,
        company: "",
        location: "",
      },
    };
  },
  methods: {
    handleFormSubmit() {
      // Add the new item to the table
      this.items.push({ ...this.formData });

      // Clear the form data
      this.formData = {
        name: "",
        type: "",
        asset: null,
        company: "",
        location: "",
      };

      // Close the modal
      this.showModal = false;
    },
  },
};
</script>

<style scoped>

</style>
