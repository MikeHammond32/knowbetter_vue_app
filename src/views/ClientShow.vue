<template>
  <div class="home">
    <h1>{{ Clients }}</h1>
    <div>
      <h2>First Name: {{ client.first_name }}</h2>
      <h2>Last Name: {{ client.last_name }}</h2>
      <h2>Location: {{ client.location }}</h2>
    </div>
  </div>
</template>

<style>
</style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      message: "Welcome to Client Show!",
      shoe: {}
    };
  },
  created: function() {
    console.log('in the create)');
    axios.get('/api/clients/' + this.$route.params.id).then(response => {
      console.log(response.data);
      this.client = response.data;
    });
  },
  methods: {}
};
</script>