<template>
  <div class="container">
    <div class="banner">
      <div id="carousel-example-generic" class="carousel slide">
  
        <!-- Wrapper for slides -->
        <div class="carousel-inner">
          <div class="item active">
            <img src="img/banner-image.jpg" alt="">
            <div class="carousel-caption">
              <h1>Morbi semuis</h1>
              <h2>Praesent dapibus, neque id cursus faucibus tortas augue eu vulputate</h2>
              <a href="#" class="btn">facilis</a>
            </div>
          </div>
          <div class="item">
            <img src="img/banner-image.jpg" alt="">
            <div class="carousel-caption">
              <h1>Morbi semuis</h1>
              <h2>Praesent dapibus, neque id cursus faucibus tortas augue eu vulputate</h2>
              <a href="#" class="btn">facilis</a>
            </div>
          </div>
          <div class="item">
            <img src="img/banner-image.jpg" alt="">
            <div class="carousel-caption">
              <h1>Morbi semuis</h1>
              <h2>Praesent dapibus, neque id cursus faucibus tortas augue eu vulputate</h2>
              <a href="#" class="btn">facilis</a>
            </div>
          </div>
        </div>

      <!-- Controls -->
      <a class="left carousel-control" href="#carousel-example-generic" data-slide="prev">
        <i class="fw-icon-chevron-left"></i>
      </a>
      <a class="right carousel-control" href="#carousel-example-generic" data-slide="next">
        <i class="fw-icon-chevron-right"></i>
      </a>
    </div>
    </div>
    <div class="container">
      <div class="featured-block">
        <!-- Example row of columns -->
        <div class="row">
          <div class="block col-md-3">
            <h1></h1>
            <h1>New User</h1>
            <div>
              <p>First Name: <input type="text" v-model="newUserFirstName"></p>
              <p>Last Name: <input type="text" v-model="newUserLastName"></p>
              <p>Phone Number: <input type="text" v-model="newUserPhoneNumber"></p>
              <p>Location: <input type="text" v-model="newUserLocation"></p>
              <p>Bio: <input type="text" v-model="newUserBio"></p>
              <p>Profession: <input type="text" v-model="newUserProfession"></p>
              <p>Password: <input type="text" v-model="newUserPassword"></p>
              <p>Email: <input type="text" v-model="newUserEmail"></p>
              <button v-on:click="createUser()">Create user</button>
            </div>
          </div>
            
          </div>
          
        </div> 
        <div class="ruler"></div>  
        </div>
        <div class="container">
          <div class="featured-item">
            <div class="col-md-6">
            <div class="block">
              <div class="block-title">
                <h1>Cras ornare tristi</h1>
                <h2>Vivamus vestibulum nulla nec ante  pellentesque</h2>
              </div>
              <ul>
                <li class="col-md-6"> 
                  <div class="user-info">
                    <i class="fw-icon-user icon"></i>
                    <h1>Tim nulla nec </h1>    
                    <p>Cuibstui ipsum dolor sit amet, consectetu</p>
                 </div>
               </li>
                <li class="col-md-6">
                  <div class="user-info">
                    <i class="fw-icon-pencil icon"></i>
                    <h1>Vivamus mol</h1>    
                    <p>Phasellus ultrices nulla quis nibh lorem</p>
                 </div>
                </li>
                <li class="col-md-6">
                  <div class="user-info">
                    <i class="fw-icon-tag icon"></i>
                    <h1>Phas ellus</h1>    
                    <p>Aliquam erat volutpat. Nam dui mi, tinci</p>
                 </div>
                </li>
                <li class="col-md-6">
                  <div class="user-info">
                    <i class="fw-icon-wrench icon"></i>
                    <h1>Fusce lobortis</h1>    
                    <p>Class aptent taciti sociosqu ad litora</p>
                 </div>
                </li>
                <li class="col-md-6">
                  <div class="user-info">
                    <i class="fw-icon-umbrella icon"></i>
                    <h1>Sed adipiscing</h1>    
                    <p class="last space">Praesent dapibus, neque id cursus</p>
                 </div>
                </li>
                <li class="col-md-6">
                  <div class="user-info">
                    <i class="fw-icon-coffee icon"></i>
                    <h1>Nam convallis</h1>    
                    <p class="last">Lorem ipsum dolor sit amet, consectetuer </p>
                 </div>
                </li>
              </ul>
            </div>
            </div>
            <div class="col-md-6">
              <div class="block">
                <div class="block-title">
                    <h1>Aliquam tincidunt</h1>
                    <h2>Integer vitae libero ac risus egestas placerat</h2>
                </div>
                  <div class="panel-group" id="accordion">
                    <div class="panel panel-default">
                      <div class="panel-heading accordion-caret">
                        <h4 class="panel-title">
                          <a class="accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseOne">
                            Donec quis dui at dolor tempor
                          </a>
                        </h4>
                      </div>
                      <div id="collapseOne" class="panel-collapse collapse in">
                        <div class="panel-body">Morbi in sem quis dui placerat ornare. Pellentesque odio nisi, euismod in, pharetra 
                                      ultricies in, diam. Sed arcu. Cras consequat.</div>
                      </div>
                    </div>

                    <div class="panel panel-default">
                      <div class="panel-heading accordion-caret">
                        <h4 class="panel-title">
                          <a class="accordion-toggle collapsed" data-toggle="collapse" data-parent="#accordion" href="#collapseTwo">
                            Vivamus molestie gravida turpis
                          </a>
                        </h4>
                      </div>
                      <div id="collapseTwo" class="panel-collapse collapse">
                        <div class="panel-body">Morbi in sem quis dui placerat ornare. Pellentesque odio nisi, euismod in, pharetra 
                                      ultricies in, diam. Sed arcu. Cras consequat.</div>
                      </div>
                    </div>

                    <div class="panel panel-default">
                      <div class="panel-heading accordion-caret">
                        <h4 class="panel-title">
                          <a class="accordion-toggle collapsed" data-toggle="collapse" data-parent="#accordion" href="#collapseThree">
                            Fusce lobortis lorem at ipsum semper 
                          </a>
                        </h4>
                      </div>
                      <div id="collapseThree" class="panel-collapse collapse">
                        <div class="panel-body">Morbi in sem quis dui placerat ornare. Pellentesque odio nisi, euismod in, pharetra 
                                      ultricies in, diam. Sed arcu. Cras consequat.</div>
                      </div>
                    </div>

                    <div class="panel panel-default">
                      <div class="panel-heading accordion-caret">
                        <h4 class="panel-title">
                          <a class="accordion-toggle collapsed" data-toggle="collapse" data-parent="#accordion" href="#collapseFour">
                            Nam convallis pellentesque nisl
                          </a>
                        </h4>
                      </div>
                      <div id="collapseFour" class="panel-collapse collapse">
                        <div class="panel-body">Morbi in sem quis dui placerat ornare. Pellentesque odio nisi, euismod in, pharetra 
                                      ultricies in, diam. Sed arcu. Cras consequat.</div>
                      </div>
                    </div>
                </div>
              </div>
            </div>
          </div>
          <div class="ruler"></div>
        </div>
      <div class="container">
        <div class="featured-content">
          <div class="col-md-6">
            <div class="block">
              <img src="img/img5.jpg" alt="" class="img-spacing thumbnail">
              <h1>Quisque a lectus. Donec consectetuer ligua </h1>
              <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Phasellus hendrerit. lentesque aliquet nibh nec urna. In nisi neque, aliquet vel, dapibus id, mattis vel, nisi. Sed pretium, ligula sollicitudin  laoreet viverra.
              </p>
              <p>Sed egestas, ante et vulputate volutpat, eros pede semper est, vitae luctus metus libero eu augue. Morbi purus libero, faucibus adipiscing, commodo quis, gravida id, est. Sed lectus. Praesent elementum hendrerit tortor. Sed semper lorem at felis.
              </p>
              <a href="#" class="btn">more</a>
            </div>            
          </div>
          <div class="col-md-6">
            <div class="block">
              <img src="img/img6.jpg" alt="" class="img-spacing thumbnail">
              <h1>Sed adipiscing ornare risus Morbi est est</h1>
              <p>Cupsim  ipsum dolor sit amet, consectetuer adipiscing elit. Phasellus hendrerit. lentesque aliquet nibh nec urna.In nisi neque, aliquet vel, dapibus id, mattis vel, nisi. Sed pretium, ligula     sollicitudi.</p>
              <p>Vivamus ante et vulputate volutpat, eros pede semper est, vitae luctus metus libero eu augue. Morbi purus libero, faucibus adipiscing, commodo quis, gravida id, est. Sed lectus. Praesent elementum hendrerit tortor. Sed semper lorem at felis.</p>
              <a href="#" class="btn">more</a>
            </div>            
          </div>
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
    console.log('the theme is loading')
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

