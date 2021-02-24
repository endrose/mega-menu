<template>
  <div id="app" class="antialiased bg-gray-800">
    <header
      class="border-t-4 border-blue-300 bg-white z-10 absolute w-full shadow-md"
    >
      <nav
        class="container mx-auto px-8 inset-0 flex flex-wrap justify-between items-center py-4"
      >
        <div class="mb-0 lg:mb-2 xl:mb-0">
          <a href="#" class="flex font-bold text-xl items-end">
            <img src="./assets/vue.png" alt="brand" class="w-10" />
            <span>ue</span>
          </a>
        </div>
        <div class="block lg:hidden">
          <button
            @click="toggle"
            type="button"
            class="flex items-center px-3 py-2 border focus:outline-none rounded border-gray-500 hover:text-gray-600 hover:border-gray-600"
          >
            <svg
              class="current-color h-3 w-3"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"
                fill="gray"
              />
            </svg>
          </button>
        </div>
        <ul
          :class="isOpen ? 'block' : 'hidden'"
          class="tracking-wide uppercase font-bold w-full block flex-grow lg:flex lg:flex-initial lg:w-auto items-center mt-8 lg:mt-0 transition duration-200 "
        >
          <li class="px-4 mb-6 text-center hover:text-gray-400 lg:mb-0">
            <a href="#">home</a>
          </li>
          <li class="px-4 mb-6 text-center hover:text-gray-400 lg:mb-0">
            <a href="#">about</a>
          </li>
          <li class="px-4 mb-6 text-center hover:text-gray-400 lg:mb-0">
            <a href="#">services</a>
          </li>
          <li class="px-4 mb-6 text-center hover:text-gray-400 lg:mb-0">
            <a href="#">skills</a>
          </li>
        </ul>
      </nav>
    </header>
    <div class="bg-gray-100 min-h-screen pt-40 text-lg"></div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "App",
  components: {},
  setup() {
    const isOpen = ref(false);
    function toggle() {
      isOpen.value = !isOpen.value;
      console.log("ok");
    }
    return {
      toggle,
      isOpen
    };
  }
};
</script>

