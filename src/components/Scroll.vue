<template>
  <div class="overflow-y-scroll h-100 p-10 w-full border-2 rounded-lg">
    <slot>Loading</slot>
  </div>
</template>

<script>
export default {
  name: "Scroll"
};
</script>

<style scoped>
.h-100 {
  height: 75%;
}
</style>
