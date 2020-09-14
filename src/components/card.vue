<template>
  <div class="card">
    <img v-bind:src="person_data.first_name" alt="img"/>
    <p class="card-id">Id: {{person_data.id}}</p>
    <p class="last_name">Name: {{person_data.last_name}}</p>
    <p class="email">Email: {{person_data.email}}</p>
    <p class="gender">Gender: {{person_data.gender}}</p>
    <p class="ip_address">IP: {{person_data.ip_address}}</p>
  </div>
</template>

<script>
export default {
  name: "card",
  props: {
    person_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  data() {
    return ;
  },
};
</script>

<style>
.card {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 #e0e0e0;
  padding: 16px;
  margin-bottom: 16px;
  width: 40%;
  height: 40%;
}
.card-id {
  font-weight: bold;
}
</style>