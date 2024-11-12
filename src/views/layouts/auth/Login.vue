<template>
  <div class="w-full h-screen">
    <div class="flex shadow rounded-md h-screen">
      <div class="bg-white dark:bg-gray-900 w-full">
        <form @submit.prevent="handleSubmit">
          <div
            class="form-body lg:max-w-[50%] mx-auto lg:p-16 p-8 lg:mt-20 mt-5 space-y-8"
          >
            <div
              class="form-head cursor-pointer"
              @click="$router.push('/')"
            >
              <img
                src="../../../assets/logo/logo.svg"
                alt=""
                class="w-10"
              />
            </div>
            <div class="space-y-3">
              <h2 class="dark:text-white font-semibold text-gray-800 text-4xl">
                Welcome, to Minstats<span class="text-primary">.</span>
              </h2>
              <p class="dark:text-gray-400 text-gray-700">
                Please enter your account to continue.
              </p>
            </div>
      
            <div class="space-y-5">
              <div class="relative z-0 w-full mb-6 group">
                <input
                  type="email"
                  v-model="email"
                  name="floating_email"
                  id="floating_email"
                  class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-primary focus:outline-none focus:ring-0 focus:border-primary peer"
                  placeholder=" "
                  required
                />
                <label
                  for="floating_email"
                  class="peer-focus:font-medium absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-primary peer-focus:dark:text-primary peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                  >Email address</label
                >
              </div>
              <div class="relative z-0 w-full mb-6 group">
                <input
                  type="password"
                  v-model="password"
                  name="floating_password"
                  id="floating_password"
                  class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-primary focus:outline-none focus:ring-0 focus:border-primary peer"
                  placeholder=" "
                  required
                />
                <label
                  for="floating_password"
                  class="peer-focus:font-medium absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-primary peer-focus:dark:text-primary peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                  >Password</label
                >
              </div>
            </div>

            <button
              type="submit"
              class="text-white bg-primary hover:bg-primary/80 p-3 w-full rounded-md"
            >
              Login, to continue
            </button>
            <p class="dark:text-white text-center text-gray-700">
              Don't have an account?<button
                type="button"
                @click="$router.push('/auth/register')"
                class="ml-2 text-primary"
              >
                Register here
              </button>
            </p>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: "Login",
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    async handleSubmit() {
      try {
        const response = await axios.post("/api/login", {
          email: this.email,
          password: this.password,
        });
        
        console.log("Login Successful:", response.data);
        
      } catch (error) {
        console.error("Login Error:", error);
      }
    },
  },
};
</script>

<style scoped>
/* Custom styles for this component */
.bg-wave {
  background: radial-gradient(
      circle at top left,
      transparent 25%,
      #4f46e5 25.5%,
      #4f46e5 36%,
      transparent 37%,
      transparent 100%
    ),
    radial-gradient(
      circle at bottom right,
      transparent 34%,
      #4f46e5 34.5%,
      #4f46e5 45.5%,
      transparent 46%,
      transparent 100%
    );
  background-size: 6em 6em;
  opacity: 1;
}
</style>
