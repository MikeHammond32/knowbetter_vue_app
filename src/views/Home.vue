<template>
  <div class="container">
        <h1>New Client</h1>
    <div>
      Name: <input type="text" v-model="newClientName">
      Width: <input type="text" v-model="newClientWidth">
      Height: <input type="text" v-model="newClientHeight">
      <button v-on:click="createClient()">Create client</button>
    </div>
    <h1>All Clients</h1>
    <div v-for="client in clients">
      <h2>{{ client.name }}</h2>
      <img v-bind:src="client.url">
      <p>Width: {{ client.width }}</p>
      <p>Height: {{ client.height }}</p>
    </div>
  </div>
</template>

<style>
</style>

<script>
import axios from "axios";


<script>
import axios from "axios";

export default {
  data: function() {
    return {
      photos: [],
      currentPhoto: {},
      newPhotoName: "",
      newPhotoWidth: "",
      newPhotoHeight: ""
    };
  },
  created: function() {
    axios.get("/api/photos").then(response => {
      this.photos = response.data;
    });
  },
  methods: {
    createPhoto: function() {
      var params = {
        name: this.newPhotoName,
        width: this.newPhotoWidth,
        height: this.newPhotoHeight
      };
      axios.post("/api/photos", params).then(response => {
        this.photos.push(response.data);
        this.newPhotoName = "";
        this.newPhotoWidth = "";
        this.newPhotoHeight = "";
      });
    },
    showPhoto: function(photo) {
      if (this.currentPhoto === photo) {
        this.currentPhoto = {};
      } else {
        this.currentPhoto = photo;
      }
    }
  }
};
</script>


