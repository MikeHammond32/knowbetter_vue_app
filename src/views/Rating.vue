<template>
  <div class="rating">
        <h1>New Rating</h1>
    <div>
      Workease(1-10): <input type="text" v-model="newRatingWorkease">
      Reliability of Payment(1-10): <input type="text" v-model="newRatingPayment">
      Comment: <input type="text" v-model="newRatingComment">
      <select>
        <option value="volvo">Mary Jackson</option>
        <option value="saab">Jim Hopper</option>
        <option value="mercedes">Larry James</option>
        <option value="audi">Lee Sin</option>
        <option value="audi">James Brown</option>
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