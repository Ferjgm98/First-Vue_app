<template>
  <div id="app" class="bg-blue-light h-screen overflow-y-hidden">
    <h1 class="font-sans text-grey-darkest text-5xl font-bold text-center pt-10">Robofriends</h1>
    <SearchBox v-on:inputChange="filterRobots"/>
    <Scroll>
      <CardList v-bind:robots="store.filteredRobots ? store.filteredRobots : robots"/>
    </Scroll>
  </div>
</template>

<script>
import SearchBox from "./components/SearchBox";
import CardList from "./components/CardList";
import Scroll from "./components/Scroll";

export default {
  name: "app",
  components: {
    SearchBox,
    CardList,
    Scroll
  },
  data() {
    return {
      robots: "",
      store: {
        filteredRobots: null
      }
    };
  },
  methods: {
    filterRobots(val) {
      this.store.filteredRobots = this.robots.filter(robot =>
        robot.name.toLowerCase().includes(val.toLowerCase())
      );
    }
  },
  created() {
    fetch("https://jsonplaceholder.typicode.com/users")
      .then(resp => resp.json())
      .then(data => (this.robots = data))
      .catch(error => {
        throw error;
      });
  }
};
</script>

<style>
</style>
