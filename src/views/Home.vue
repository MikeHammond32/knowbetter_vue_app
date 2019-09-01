<template>
  <div class="container">
        <h1>New User</h1>
    <div>
      First Name: <input type="text" v-model="newUserFirstName">
      Last Name: <input type="text" v-model="newUserLastName">
      Phone Number: <input type="text" v-model="newUserPhoneNumber">
      Location: <input type="text" v-model="newUserLocation">
      Bio: <input type="text" v-model="newUserBio">
      Profession: <input type="text" v-model="newUserProfession">
      Password: <input type="text" v-model="newUserPassword">
      Email: <input type="text" v-model="newUserEmail">
      <button v-on:click="createUser()">Create user</button>
    </div>
    <router-link to="/login">Login</router-link>
    <h1>All Users</h1>
    <div v-for="user in users">
      <h2>{{ user.FirstName }}</h2>
      <img v-bind:src="user.url">
      <button v-on:click="showUser(user)">Show more</button>
      <div v-if="currentUser === user">
        <p>FirstName: {{ user.FirstName }}</p>
        <p>LastName: {{ user.LastName }}</p>      
        <p>PhoneNumber: {{ user.PhoneNumber }}</p>
        <p>Location: {{ user.Location }}</p>
        <p>Bio: {{ user.Bio }}</p>
        <p>Profession: {{ user.Profession }}</p>
        <p>Password: {{ user.Password }}</p>
        <p>Email: {{ user.Email }}</p>
      </div>
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
      newUserProfession: "",
      newUserPassword: "",
      newUserEmail: ""
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
        first_name: this.newUserName,
        last_name: this.newUserWidth,
        phone_number: this.newUserPhoneNumber,
        location: this.newUserLocation,
        bio: this.newUserBio,
        profession: this.newUserProfession,
        password: this.newUserPassword,
        email: this.newUserEmail
      };
      axios.post("/api/users", params).then(response => {
        this.users.push(response.data);
        this.newUserFirstName = "";
        this.newUserLastName = "";
        this.newUserPhoneNumber = "";
        this.newUserLocation = "";
        this.newUserBio = "";
        this.newUserProfession = "";
        this.newUserPassword = "";
        this.newUserEmail = "";
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

