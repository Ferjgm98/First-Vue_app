<template>
  <div class="w-full flex items-center content-center justify-center flex-wrap my-12 md:mx-auto">
    <Card v-for="(robot, i) in robots" v-bind:key="i" v-bind:robot="robot"/>
  </div>
</template>

<script>
import Card from "./Card";

export default {
  name: "CardList",
  props: ["robots"],
  components: {
    Card
  }
};
</script>

<style scoped>
</style>
