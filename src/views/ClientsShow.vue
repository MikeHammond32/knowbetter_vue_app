<template>
  <div class="home">
    <h1>First Name: {{ client.first_name }} </h1>
    <h1>Last Name: {{ client.last_name}} </h1>
    <h1>Location: {{ client.location }} </h1> 
    <div v-for="rating in client.ratings">
      <p>Comment: {{rating.comment}}</p> Workease: {{rating.workease}} Reliability of Payment: {{rating.payment}}
    </div>
    <div>
<!--       <h2>First Name: {{ client.first_name }}</h2>
      <h2>Last Name: {{ client.last_name }}</h2>
      <h2>Location: {{ client.location }}</h2> -->
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
      message: "Welcome to Show!",
      client: {}
    };
  },
  created: function() {
    // console.log(this.$route.params.id);
    axios.get('/api/clients/' + this.$route.params.id).then(response => {
      console.log(response.data);
      this.client = response.data;
    })
    // console.log('in the create)');
    // axios.get('/api/clients/1' + this.$route.params.id).then(response => {
    //   console.log(response.data);
    //   this.client = response.data;
    // });
  },
  methods: {}
};
</script>