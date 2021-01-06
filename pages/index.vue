<template>
  <main class="container mx-auto px-4 bg-handy-black">
    <section class="pt-12 md:pt-20 pb-6 px-2">
      <div class="flex flex-wrap text-center lg:text-left">
        <div class="lg:w-1/2 px-2 lg:pr-10 mt-10 lg:mt-0 order-1 lg:order-none">
          <h1
            class="text-4xl md:text-5xl mb-6 leading-tight font-heading text-handy-red font-semibold"
          >
            {{ ToolTitle }}
          </h1>
          <p class="mb-8 text-white leading-relaxed">
            {{ ToolDescription }}
          </p>
          <form @submit.prevent="submit" class="w-full max-w-xl mx-auto">
            <!-- form -->
            <div class="flex flex-wrap mb-4">
              <div class="w-full md:w-2/3">
                <input
                  v-model="connectionKey"
                  :disabled="submitted"
                  class="appearance-none placeholder-gray-800 block w-full py-3 px-4 mb-4 md:mb-0 leading-snug text-gray-700 bg-gray-200 focus:bg-white border border-gray-200 focus:border-gray-500 rounded-full md:rounded-r-none focus:outline-none"
                  type="text"
                  required
                  placeholder="Your connection key"
                  aria-label="Nettadresse"
                />
              </div>
              <div class="w-full md:w-1/3">
                <button
                  :disabled="submitted"
                  name="submit"
                  type="submit"
                  class="inline-block font-medium w-full py-4 px-8 leading-none text-white bg-handy-red hover:bg-red-700 rounded-full md:rounded-l-none"
                >
                  Connect
                </button>
              </div>
                           <div
                v-if="formerror"
                aria-live="polite"
                class="mt-4 text-red-700"
              >
                ❌ {{ formerror }}. Try gain.
              </div>

              <div
                v-if="data && !formerror"
                aria-live="polite"
                class="mt-4 text-green-500"
              >
                ✔️ You're connected
              </div>
            </div>
            </p>
          </form>
          <!-- form -->
        </div>
        <div class="mx-auto w-full lg:w-1/2 px-2 max-w-xs lg:max-w-none">
          <img
            src="~/assets/svg/login.svg"
            alt=""
            width="907"
            height="671.95"
          />
        </div>
      </div>
    </section>
  </main>
</template>

<script>

export default {
  data() {
    return {
      ToolTitle: 'Connect',
      ToolDescription:
        'Enter your connection key and connect..',
      submitted: false,
      connectionKey: '',
      data: '',
      resultTitle: '',
      dataLoading: '',
      dataLoadingSpinner: '',
      results: '',
      formerror: this.formerror,

    }
  },

  methods: {
    async submit() {


        // Store connection key to UX here
        this.submitted = false
        this.data = "ok"
    
    },
  },
}
</script>
