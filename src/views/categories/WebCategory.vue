<template>
  <div class="flex justify-center">
    <div class="w-[90%] text-white mt-20 h-[70vh]">
      <div class="flex justify-end">
        <button
          type="button"
          @click="showModal = true"
          class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-10 py-4 mr-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"
        >
          Add Category Dimension
        </button>
      </div>
      <div class="flex justify-between mt-20">
        <div>
          <h1
            class="text-2xl font-semibold mb-2 text-gray-900 dark:text-gray-200"
          >
            Web Development Category
          </h1>
          <p class="mb-4 dark:text-yellow-400 text-black">
            You can also invert the colors—with light text on dark backgrounds.
          </p>
        </div>

        <!-- Add Category Dimension Button -->
      </div>

      <!-- Table -->
      <table
        class="table-auto w-full text-sm text-left text-gray-500 dark:text-gray-400 lg:overflow-auto overflow-x-scroll"
      >
        <thead
          class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400"
        >
          <tr class="">
            <th class="px-4 py-8">Name</th>
            <th class="px-4 py-8">Types</th>
            <th class="px-4 py-8">Descrition</th>
            <th class="px-4 py-8">Values</th>
            <th class="px-4 py-8">Order</th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="(item, index) in items"
            :key="index"
            class="bg-white border-b dark:bg-gray-800 dark:border-gray-900 odd:bg-white even:bg-gray-50"
          >
            <td class="px-4 py-8">{{ item.name }}</td>
            <td class="px-4 py-8">{{ item.type }}</td>
            <td class="px-4 py-8">{{ item.description }}</td>
            <td class="px-4 py-8">{{ item.values }}</td>
            <td class="px-4 py-8">{{ item.order }}</td>
          </tr>
        </tbody>
      </table>

      <!-- Modal Form -->
      <div
      v-if="showModal"

        class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center"
      >
        <div class="bg-white text-black p-6 rounded-md w-full max-w-[70%]">
          <div class="grid grid-cols-1 justify-center mb-8">
            <h2 class="text-[40px] text-center font-bold mb-4">Add Category Dimension
            </h2>
            <p class="text-center">
              Add another statistics for your categories services
            </p>
          </div>

          <form @submit.prevent="handleFormSubmit">
            <div class="grid grid-cols-2 gap-4">
              <!-- Name -->
              <div class="mb-4">
                <label class="block text-sm font-medium">Dimension Name</label>
                <input
                  v-model="formData.name"
                  type="text"
                  class="w-full p-2 border border-gray-300 rounded-md"
                  required
                />
              </div>
              
              <!-- Description -->
              <div class="mb-4">
                <label class="block text-sm font-medium">Description</label>
                <input
                v-model="formData.description"
                type="text"
                class="w-full p-2 border border-gray-300 rounded-md"
                required
                />
              </div>
              
              <!-- Type -->
              <div class="mb-4">
                <label class="block text-sm font-medium">Input Type</label>
                <input
                v-model="formData.type"
                  type="number"
                  class="w-full p-2 border border-gray-300 rounded-md"
                  required
                />
              </div>

              <!-- Display as -->
              <div class="mb-4">
                <label class="block text-sm font-medium">Display as</label>
                <input
                  v-model="formData.display"
                  type="text"
                  class="w-full p-2 border border-gray-300 rounded-md"
                  required
                />
              </div>

              <!-- order -->
              <div class="mb-4">
                <label class="block text-sm font-medium">Possible values</label>
                <input
                  v-model="formData.value"
                  type="text"
                  class="w-full p-2 border border-gray-300 rounded-md"
                  required
                />
              </div>
              <div class="mb-4">
                <label class="block text-sm font-medium">Order</label>
                <input
                  v-model="formData.order"
                  type="text"
                  class="w-full p-2 border border-gray-300 rounded-md"
                  required
                />
              </div>
            </div>

            <div class="flex justify-end space-x-2 mt-4">
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
                Add Dimension
              </button>
            </div>
          </form>
        </div>
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
          description: 7634825,
          values: "Blue Riband",
          order: "California",
        },
        {
          name: "Jarvis Pepperspray",
          type: "Treenut",
          description: 8421678,
          values: "Burton's Maryland Specials",
          order: "Massachusetts",
        },
        {
          name: "Phillip Anthropy",
          type: "Sweetener",
          description: 8462150,
          values: "Quaker Instant Oatmeal",
          order: "Illinois",
        },
        {
          name: "Alan Fresco",
          type: "Dairy",
          description: 8741632,
          values: "Disney Pixar Milk Chocolate Crispy Bars",
          order: "Michigan",
        },
      ],

      // Modal control and form data
      showModal: false,
      formData: {
        name: "",
        description: "",
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
        description: "",
      };

      // Close the modal
      this.showModal = false;
    },
  },
};
</script>

<style scoped></style>
