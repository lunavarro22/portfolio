<template>
  <section class="text-gray-400 body-font ml-auto mr-auto w-2/5 md:w-4/5">
    <div
      class="container mx-auto flex px-5 py-10 md:flex-row flex-col items-center"
    >
      <div class="md:w-2/6 w-5/6 md:mb-0 mb-10 text-center">
        <fa class="text-6xl contact-icon" :icon="['fas', 'phone']" />
      </div>
      <div
        class="lg:flex-grow md:w-1/2 lg:pl-24 md:pl-16 flex flex-col md:items-start md:text-left items-center text-center"
      >
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-white">
          Feel free to mail me.
        </h1>
        <div class="flex justify-center">
          <a href="mailto:lunavarro@csumb.edu" target="_blank">
            <button
              class="inline-flex ml-4 border-2 border-red-500 text-white bg-red-900 border-0 py-2 px-6 focus:outline-none hover:bg-red-500 rounded-full text-lg"
            >
              Message <fa :icon="['fas', 'envelope']" class="my-auto ml-2" />
            </button>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
p {
  font-family: "Poppins", sans-serif;
}

h1 {
  font-family: "Poppins", sans-serif;
}

@media (min-width: 768px) {
  .contact-icon {
    font-size: 12rem;
  }
}
</style>
