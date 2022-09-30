<template>
  <div>
    <Header :headline="headline" :name="name" :tags="tags" />
    <intro />
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import Intro from "../components/Intro.vue";

export default {
  components: {
    Header,
    Intro,
  },
  data() {
    return {
      headline: "Hello! I am",
      name: "Luis Navarro",
      tags: [
        "#Network Administrator",
        "#Database Administrator",
        "#Manager",
        "#Frontend Developer",
      ],
    };
  },
};
</script>

<style>
</style>
