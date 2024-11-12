<template>
  <div class="flex justify-center">

    <div class="  w-[90%] bg-gray-900 text-white mt-20 h-[70vh]">
  
      <div class="flex justify-end">
  
        <button
          @click="showModal = true"
          class="bg-blue-500 hover:bg-blue-600 text-white py-2 px-4 rounded-md"
        >
          Add Category Dimension
        </button>
      </div>
      <div class="flex justify-between mt-20">
        <div>
          <h1 class="text-2xl font-semibold mb-2">Web Development Category</h1>
          <p class="mb-4 text-gray-400">
            You can also invert the colors—with light text on dark backgrounds.
          </p>
        </div>
  
        <!-- Add Category Dimension Button -->
      </div>
  
      <!-- Table -->
      <table class="table-auto w-full mt-4 text-gray-300">
        <thead>
          <tr class="border-b border-gray-700">
            <th class="px-4 py-8">Name</th>
            <th class="px-4 py-8">Types</th>
            <th class="px-4 py-8">Asset</th>
            <th class="px-4 py-8">Company</th>
            <th class="px-4 py-8">Location</th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="(item, index) in items"
            :key="index"
            class="border-b border-gray-800"
          >
            <td class="px-4 py-8">{{ item.name }}</td>
            <td class="px-4 py-8">{{ item.type }}</td>
            <td class="px-4 py-8">{{ item.asset }}</td>
            <td class="px-4 py-8">{{ item.company }}</td>
            <td class="px-4 py-8">{{ item.location }}</td>
          </tr>
        </tbody>
      </table>
  
      <!-- Modal Form -->
      <div
        v-if="showModal"
        class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center"
      >
        <div class="bg-white text-black p-6 rounded-md w-full max-w-[70%]">
          <div class="grid grid-cols-1 first-letter:justify-center mb-8">

            <h2 class="text-[40px] text-center font-bold mb-4">Add Category </h2>
            <p class="text-center">Add another statistics for your categories services</p>
          </div>
  
          <form @submit.prevent="handleFormSubmit">
            <div class="mb-4">
              <label class="block text-sm font-medium">Category Name</label>
              <input
                v-model="formData.name"
                type="text"
                class="w-full p-2 border border-gray-300 rounded-md"
                required
              />
            </div>
  
            <div class="mb-4">
              <label class="block text-sm font-medium">Description</label>
              <textarea 
                v-model="formData.description" 
                class="w-full p-2 border border-gray-300 rounded-md" 
                rows="3" 
                placeholder="Enter a description"
                required
              ></textarea>
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

<style scoped>

</style>
