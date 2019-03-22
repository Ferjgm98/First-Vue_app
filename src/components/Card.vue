<template>
  <div
    class="card-hover group rounded overflow-hidden shadow-lg my-1 px-1 mx-2 overflow-hidden sm:my-3 sm:px-3 bg-grey-lighter hover:bg-grey-light"
  >
    <img v-bind:src="`https://robohash.org/robot-${robot.id}?200x200`" alt="robot" class="max-w">
    <div class="px-6 py-10">
      <h2 class="font-bold text-black text-xl mb-2 text-center">{{ robot.username }}</h2>
      <p class="text-grey-darker text-base text-center">{{ robot.email }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["robot"]
};
</script>

<style scoped>
.card-hover {
  transition: all 0.2s ease-in-out;
}
.card-hover:hover {
  transform: scale(1.1);
}
</style>
