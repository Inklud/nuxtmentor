<template>
  <nav class="bg-handy-black">
    <div class="flex flex-wrap items-center justify-between container mx-auto px-8 py-4">
    <div class="flex flex-shrink-0">
      <n-link
        to="/" style="font-size: 1.43rem"
        class="text-2xl font-bold text-handy-red"
      >Connect</n-link>
    </div>
    <div class="block lg:hidden">
      <button
        @click="menu = !menu"
        class="navbar-burger flex items-center py-1 px-2 text-white"
      >
        <svg
          v-show="menu == true"
          class="fill-current h-6 w-6 text-white"
          viewbox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Open menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
        </svg>

        <svg
          v-show="menu == false"
          class="fill-current h-6 w-6 text-white" 
          viewbox="0 0 24 24"
          width="20"
          height="20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Close menu</title>
          <path d="M19 6.41L17.59 5L12 10.59L6.41 5L5 6.41L10.59 12L5 17.59L6.41 19L12 13.41L17.59 19L19 17.59L13.41 12L19 6.41z"></path>
        </svg>
        <span class="ml-2" style="margin-top: -1.5px">Menu</span>
      </button>
    </div>

    <div
      v-show="menu == true"
      class="hidden navbar-menu lg:flex lg:flex-grow lg:items-center w-full lg:w-auto"
    >
      <div class="lg:mr-auto font-medium">
      </div>
      <div class="font-medium">
        <n-link 
          to="/remote/"
          class="block lg:inline-block mt-4 lg:mt-0 lg:mr-8 text-white hover:underline hover:text-white"
        >Remote</n-link>
        <n-link 
          to="/"
          class="inline-block pt-3 pb-3 px-6 mt-4 lg:mt-0 leading-none text-white rounded-full shadow bg-handy-red hover:bg-red-700"
        >Connect</n-link>
      </div>
    </div>

    <!-- Mobile menu -->
    <div
      v-show="menu == false"
      @click="menu = !menu"
      class="navbar-menu lg:flex lg:flex-grow lg:items-center w-full lg:w-auto"
    >
      <div class="lg:mr-auto font-medium">
      </div>
      <div class="font-medium">
        <n-link 
          to="/remote/"
          class="block lg:inline-block mt-4 lg:mt-0 lg:mr-8 text-white hover:underline hover:text-white"
        >Remote</n-link>
        <n-link
          to="/"
          class="inline-block py-3 px-6 mt-4 lg:mt-0 leading-none text-white rounded-full shadow bg-handy-red hover:bg-red-700"
        >Connect</n-link>
      </div>
    </div>
  </div>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      menu: true
    }
  },
}
</script>