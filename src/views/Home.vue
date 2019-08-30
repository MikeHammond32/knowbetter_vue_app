<template>
  <div class="home">
    <h1>All Clients</h1>
    <div v-for="client in clients">
      <h2>{{ photo.name }}</h2>
      <img v-bind:src="photo.url">
      <p>Width: {{ photo.width }}</p>
      <p>Height: {{ photo.height }}</p>
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
      message: "Welcome to Vue.js!"
    };
  },
  created: function() {
    axios.get("/api/clients").then(response => {
      this.photos = response.data;
    }); 
  },
  methods: {}
};
</script>