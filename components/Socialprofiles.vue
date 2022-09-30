<template>
  <div>
    <div class="icon-bar fixed md:ml-2">
      <a
        :href="site.link"
        v-for="site in sites"
        :key="`${site.brand}`"
        :class="[
          'block',
          'text-center',
          'p-3',
          'text-black',
          site.brand,
          'rounded-full',
          'bg-white',
          'mb-1',
          'icons',
        ]"
        target="_blank"
        ><fa :icon="['fab', site.brand]" class="text-2xl"
      /></a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sites: [
        { brand: "linkedin", link: "https://www.linkedin.com/in/luis-navaro-csumb/" },
        { brand: "github", link: "https://github.com/lunavarro22" },
      ],
    };
  },
};
</script>

<style scoped>
.icon-bar {
  top: 35%;
}

.icons {
  width: 48px;
  height: 48px;
}

.icon-bar a {
  transition: all 0.3s ease;
}

.google:hover {
  background: rgb(66, 133, 244);
  background: linear-gradient(
    90deg,
    rgba(66, 133, 244, 1) 0%,
    rgba(234, 67, 53, 1) 33%,
    rgba(251, 188, 5, 1) 66%,
    rgba(52, 168, 83, 1) 100%
  );
  color: white;
}

.linkedin {
  color: #0e76a8;
}

.linkedin:hover {
  background: #0e76a8;
  color: white;
}

.github {
  color: #000000;
}

.github:hover {
  background: #000000;
  color: white;
}
</style>
