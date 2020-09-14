<template>
  <div id="app">
    <main-wrapper :persons="persons" />
  </div>
</template>

<script>
import MainWrapper from "./components/main-wrapper";
import db from "./db.json";
export default {
  name: "App",
  components: {
    MainWrapper,
  },
  data() {
    return {
      persons: [],
    };
  },
  created() {
    this.data = db.jsonc;
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
