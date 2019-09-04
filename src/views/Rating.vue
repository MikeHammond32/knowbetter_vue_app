<template>
  <div class="rating">
        <h1>New Rating</h1>
    <div>
      Workease(1-10): <input type="text" v-model="newRatingWorkease">
      Reliability of Payment(1-10): <input type="text" v-model="newRatingPayment">
      Comment: <input type="text" v-model="newRatingComment">
      <select v-model="newRatingClientId">
        <option v-for="client in clients" v-bind:value="client.id">{{client.first_name}} {{client.last_name}}</option>
      </select>
      <button v-on:click="createRating()"> Add Rating</button>
    </div>
  </div>
</template>


<script>
import axios from "axios";

export default {
  data: function() {
    return {
      clients: [],
      currentUser: {},
      newRatingWorkease: "",
      newRatingPayment: "",
      newRatingComment: "",
      newRatingRatingId: "",
      newRatingUserId: "",
      newRatingClientId: ""
    };
  },
  created: function() {
    axios.get("/api/clients").then(response => {
      console.log(response.data)
      this.clients = response.data;
    });
  },
  methods: {
    createRating: function() {
      var params = {
        workease: this.newRatingWorkease,
        payment: this.newRatingPayment,
        comment: this.newRatingComment,
        client_id: this.newRatingClientId
      };
      axios.post("/api/ratings", params).then(response => {
        this.clients.push(response.data);
        this.newRatingWorkease = "";
        this.newRatingPayment = "";
        this.newRatingComment = "";
        this.newRatingRatingId = "";
      });
    },
    showRating: function(rating) {
      if (this.currentRating === rating) {
        this.currentRating = {};
      } else {
        this.currentRating = rating;
      }
    }
  }
};
</script>