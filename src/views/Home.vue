<template>
  <div class="container">
        <h1>New Client</h1>
    <div>
      First Name: <input type="text" v-model="newUserFirstName">
      Last Name: <input type="text" v-model="newUserLastName">
      Phone Number: <input type="text" v-model="newUserPhoneNumber">
      Location: <input type="text" v-model="newUserLocation">
      Bio: <input type="text" v-model="newUserBio">
      Profession: <input type="text" v-model="newUserProfession">
      <button v-on:click="createUser()">Create user</button>
    </div>
    <h1>All Users</h1>
    <div v-for="user in users">
      <h2>{{ user.name }}</h2>
      <img v-bind:src="user.url">
      <p>FirstName: {{ user.FirstName }}</p>
      <p>LastName: {{ user.LastName }}</p>      
      <p>PhoneNumber: {{ user.PhoneNumber }}</p>
      <p>Location: {{ user.Location }}</p>
      <p>Bio: {{ user.Bio }}</p>
      <p>Profession: {{ user.Profession }}</p>
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
      newUserFirstName: "",
      newUserLastName: "",
      newUserPhoneNumber: "",
      newUserLocation: "",
      newUserBio: "",
      newUserProfession: ""
    };
  },
  created: function() {
    axios.get("/api/users").then(response => {
      this.users = response.data;
    });
  },
  methods: {
    createUser: function() {
      var params = {
        FirstName: this.newUserName,
        LastName: this.newUserWidth,
        PhoneNumber: this.newUserPhoneNumber,
        Location: this.newUserLocation,
        Bio: this.newUserBio,
        Profession: this.newUserProfession
      };
      axios.post("/api/users", params).then(response => {
        this.users.push(response.data);
        this.newUserFirstName = "";
        this.newUserLastName = "";
        this.newUserPhoneNumber = "";
        this.newUserLocation = "";
        this.newUserBio = "";
        this.newUserProfession = "";
      });
    },
    showUser: function(user) {
      if (this.currentUser === user) {
        this.currentUser = {};
      } else {
        this.currentUser = user;
      }
    },
    updateUser: function(user) {
      var params = {
        FirstName: user.FirstName,
        LastName: user.LastName,
        PhoneNumber: user.PhoneNumber,
        Location: user.Location,
        Bio: user.Bio,
        Profession: user.Profession
      };
      axios
        .patch("/api/users/" + user.id, params)
        .then(response => {
          this.currentUser = {};
        });
    }
  }
};
</script>

