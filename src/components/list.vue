<template>
  <div class="list">
    <h1>CardsList</h1>
    <div class="list__list">
      <card v-for="person in persons" :key="person.ip_address" v-bind:person_data="person"/>
    </div>
  </div>
</template>

<script>
import card from "./card";
export default {
  name: "list",
  components: {
    card,
  },
  props: {
    persons: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style>
.list {
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  text-align: center;
}
.list__list {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}
</style>