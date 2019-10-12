<template>
  <div id="app">
    <BasePosts />
  </div>
</template>

<script>
import BasePosts from "./components/BasePosts.vue";

export default {
  name: "app",
  components: {
    BasePosts
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
