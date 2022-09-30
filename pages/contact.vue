<template>
  <div>
    <Header :headline="headline" :name="name" :tags="tags" />
    <contact />

  </div>
</template>

<script>
import Header from "../components/Header.vue";
import contact from "../components/Contact.vue";

export default {
  components: {
    Header,
    contact
  },
  data() {
    return {
      headline: "",
      name: "Contact Me!",
      tags: [
      ],
    };
  },
  head(){
    return{
      title: "Luis Navarro - Contact",
    }
  }
};
</script>

<style scoped>
</style>
