<template>
    <div class="flex justify-center">
  
      <div class="  w-[90%]  text-white mt-20 h-[70vh]">
    
        <div class="flex justify-end">
    
  
          <button
          description="button"
          @click="showModal = true"
          class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-10 py-4 mr-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"
        >
        Add Category
        </button>
        </div>
        <div class="flex justify-between mt-20">
          <div>
            <h1 class="text-2xl font-semibold mb-2 text-gray-900 dark:text-gray-200">Add Category</h1>
            <p class="mb-4 dark:text-yellow-400 text-black">
              You can also invert the colors—with light text on dark backgrounds.
            </p>
          </div>
    
          <!-- Add Category Dimension Button -->
        </div>
    
        <!-- Table -->
        <table class="table-auto w-full text-sm text-left text-gray-500 dark:text-gray-400 lg:overflow-auto overflow-x-scroll">
          <thead
           class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400"
          >
            <tr class="">
              <th class="px-4 py-8">Name</th>
              <th class="px-4 py-8">Description</th>
            </tr>
          </thead>
          <tbody>
            <tr
              v-for="(item, index) in items"
              :key="index"
            class="bg-white border-b dark:bg-gray-800 dark:border-gray-900 odd:bg-white even:bg-gray-50"
            >
              <td class="px-4 py-8">{{ item.name }}</td>
              <td class="px-4 py-8">{{ item.description }}</td>
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
                  description="text"
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
                  description="button"
                  @click="showModal = false"
                  class="bg-gray-300 hover:bg-gray-400 py-2 px-4 rounded-md"
                >
                  Cancel
                </button>
                <button
                  description="submit"
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
    name:"AddCategory",
    data() {
      return {
        // Sample data for the table
        items: [
          {
            name: "Parsley Montana",
            description: "Candy",
          },
          {
            name: "Jarvis Pepperspray",
            description: "Treenut",
          },
          {
            name: "Phillip Anthropy",
            description: "Sweetener",
          },
          {
            name: "Alan Fresco",
            description: "Dairy",
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
  