<template>
  <div class="home">
    <h1>All Clients</h1>
    <div v-for="client in clients">
      <h2>{{ client.name }}</h2>
      <img v-bind:src="client.url">
      <p>First Name: {{ client.first_name }}</p>
      <p>Last Name: {{ client.last_name }}</p>
      <p>Location: {{ client.location }}</p>
      <a v-bind:href="'/clients/' + client.id ">see more info</a>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      clients: []
    };
  },
  created: function() {
    console.log('i am in created')
    axios.get("/api/clients").then(response => {
      console.log(response.data)
      this.clients = response.data;
    });
  },
  methods: {}
};
</script>