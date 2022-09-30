<template>
  <header class="text-gray-600 body-font">
    <div
      class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"
    >
      <a
        class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0"
      >
        <img class="w-10" src="../assets/icons/logo.svg" />
        <span class="ml-3 text-xl text-white">Luis Navarro</span>
      </a>
      <nav
        class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center md:pr-32"
      >

        <nuxt-link
          :to="link == 'About' ? '/' : link"
          :class="[computedClass(link.toLowerCase()), 'mr-5', 'cursor-pointer']"
          v-for="link in links"
          :key="`${link}`"
          >{{ selectedOption(link) }}</nuxt-link
        >
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  methods: {
    computedClass(link) {
      let className = "";
      if (this.$route.name == "index" && link == "about")
        className = "text-blue-500";
      else if (this.$route.name == link) className = "text-blue-500";
      else className = "hover:text-blue-300";
      return className;
    },
    selectedOption(link) {
      let option = "";
      if (this.$route.name == "index" && link == "About")
        option = "< " + link + " >";
      else if (this.$route.name.toLowerCase() == link.toLowerCase())
        option = "< " + link + " >";
      else option = link;
      return option;
    },
  },

  data() {
    return {
      links: ["About", "Projects", "Contact"],
    };
  },
};
</script>

<style scoped>
span {
  font-family: "Pacifico", cursive;
}
</style>
