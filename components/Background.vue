<template>
  <div class="h-full fixed">
    <div class="stars">
      <Star v-for='i in 40' :key="`${i}`"/>
    </div>
  </div>
</template>

<script>
import Star from "./Dots"
export default {
  components:{
    Star,
  }
};
</script>

<style >

</style>
