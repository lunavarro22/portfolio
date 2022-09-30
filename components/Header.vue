<template>
  <div class="grid md:grid-cols-1 text-center">
    <h2 class="text-white">
      {{headline}}<span class="name text-white ml-2">{{ name }}</span>
    </h2>
    <div
      class="mt-5 flex flex-wrap w-4/5 justify-center md:w-2/5 ml-auto mr-auto"
    >
      <p
        class="rounded-xl text-base m-1 tagged inline text-white p-2 bg-black cursor-default"
        v-for="tag in tags"
        :key="`${tag}`"
      >
        {{ tag }}
      </p>
    </div>
    </div>
</template>

<script>
export default {
  props: {
    headline: String,
    name: String,
    tags: Array,
  },
};
</script>

<style scoped>
span {
  font-size: 7vh;
  font-family: "Pacifico", cursive;
}

h2 {
  font-size: 5.7vh;
  font-family: "Pacifico", cursive;
}

.name {
  animation: animated-rainbow-shadow 1s infinite;
}

.tagged {
  background: rgb(54, 116, 173);
  background: linear-gradient(
    87deg,
    rgba(54, 116, 173, 1) 0%,
    rgba(54, 96, 173, 1) 100%
  );
}
</style>
