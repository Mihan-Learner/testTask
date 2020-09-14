<template>
  <div class="main-wrapper">
    <list :persons="persons"/>
  </div>
</template>

<script>
import List from "./list";

export default {
  name: "main-wrapper",
  components: {
    List,
  },
  props: {
    persons: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  data() {
    return {
      title: "Main wrapper",
    };
  },
};
</script>

<style>
.main-wrapper {
  max-width: 900px;
  margin: 0 auto;
}
</style>