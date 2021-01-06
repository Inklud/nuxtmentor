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
        'Show the connection key below',
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
