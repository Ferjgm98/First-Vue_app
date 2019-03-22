<template>
  <div class="mx-full flex justify-center py-5">
    <input
      type="text"
      class="bg-grey-lighter appearance-none border-2 border-grey-lighter rounded w-25 py-2 px-4 text-grey-dark leading-tight focus:outline-none focus:bg-white focus:border-purple"
      placeholder="Find a robot"
      v-on:input="$emit('inputChange', $event.target.value)"
      autofocus
    >
  </div>
</template>

<script>
export default {
  name: "SearchBox"
};
</script>

<style scoped>
</style>
