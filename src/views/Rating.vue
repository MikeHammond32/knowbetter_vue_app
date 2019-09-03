<template>
  <div class="rating">
    <router-link to="/ratings">Add Rating</router-link>
        <h1>New Rating</h1>
    <div>
      Workease(1-10): <input type="text" v-model="newRatingWorkease">
      Reliability of Payment(1-10): <input type="text" v-model="newRatingPayment">
      Comment: <input type="text" v-model="newRatingComment">
      <select>
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
        <option value="mercedes">Mercedes</option>
        <option value="audi">Audi</option>
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
      users: [],
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
    axios.get("/api/ratings").then(response => {
      this.users = response.data;
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
        this.users.push(response.data);
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