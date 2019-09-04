    <router-link to="/rating">Add Rating</router-link>
    <router-link to="/clientshow">Clients</router-link>
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