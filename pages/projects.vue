<template>
  <div>
    <Header :headline="headline" :name="name" :tags="tags" />
    <Skills />

  </div>
</template>

<script>
import Header from "../components/Header.vue";
import Skills from "../components/Skills.vue";

export default {
  components: {
    Header,
    Skills,
  },
  data() {
    return {
      headline: "Hands-on experience ",
      name: "skills!",
      tags: [
        "#Database Designing",
        "#Front-end development",
      ],
    };
  },
  head(){
    return{
      title: "Luis Navarro - Projects",
    }
  }
};
</script>

<style scoped>
</style>
