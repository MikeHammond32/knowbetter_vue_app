<template>
  <div id="app">
    <div class="header-wrapper">
      <div class="site-name">
        <h1>KnowBetter</h1>
        <h2></h2>
      </div>
    </div>
    <div class="menu">
      <div class="navbar">
        <div class="container">
          <div class="navbar-header">
            <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
              <i class="fw-icon-th-list"></i>
            </button>
          </div>
          <div class="navbar-collapse collapse">
            <ul class="nav navbar-nav">
              <li><a href="/">Home</a></li>
              <li><a href="/rating">New Rating</a></li>
              <li><a href="/clientindex">Clients</a></li>
              <li><a href="/Login">Sign In</a></li>
              <li><a href="/Logout">Log out</a></li>
            </ul>
          </div><!--/.navbar-collapse -->
        </div>
      </div>
      <div class="mini-menu">
            <label>
          <select class="selectnav">
            <option value="" selected="">Home</option>
            <option value="#">About</option>
            <option value="#">→ Another action</option>
            <option value="#">→ </option>
            <option value="#">→ Another action</option>
            <option value="#">→ Something else here</option>
            <option value="#">Services</option>
            <option value="#">Work</option>
            <option value="#">Contact</option>
          </select>
          </label>
          </div>
    </div>
    <router-view />
    <!-- Main jumbotron for a primary marketing message or call to action -->

      <div class="footer-wrapper">
        <div class="site-content">
        <div class="container">
        <div class="row">
        
          <div class="block col-md-2 col-sm-6">
            <h1>Vitae lin</h1>
            <ul>
              <li><a href="#"></a></li>
              <li><a href="#"></a></li>
              <li><a href="#"></a></li>
            </ul>
          </div>
          <div class="block col-md-2 col-sm-6">
            <h1>Luctrus</h1>
            <ul>
              <li><a href="#"></a></li>
              <li><a href="#"></a></li>
              <li><a href="#"></a></li>
            </ul>
          </div>
          <div class="block col-md-2 col-sm-6">
            <h1>consetu</h1>
            <ul>
              <li><a href="#"></a></li>
              <li><a href="#"></a></li>
              <li><a href="#"></a></li>
            </ul>
          </div>
          <div class="block col-md-3">
            <h1></h1>
            <div class="input-group">
                <input type="email" value="" name="EMAIL" class="required email form-control" id="mce-EMAIL">
                <span class="input-group-btn">
              <input type="submit" class="button btn btn-default" value="Subscribe" name="subscribe" id="mc-embedded-subscribe">
                </span>
            </div> 
          </div>
          <div class="block col-md-3">
            <h1></h1>
            <ul class="social">
              <li><a href="#"><i class="fw-icon-twitter"></i></a></li>
              <li><a href="#"><i class="fw-icon-facebook"></i></a></li>
              <li><a href="#"><i class="fw-icon-linkedin"></i></a></li>
            </ul>
          </div>
        </div>
        </div>
        
      </div>
      <div class="copy-rights">
      <div class="container">
        <div class="row">
          
            <div class="col-md-6">
              Copyright(c) website name. Designed by: <a href="http://www.alltemplateneeds.com"> www.alltemplateneeds.com</a>
            </div>
            <div class="col-md-6">
              Images from: <a href="http://www.wallpaperswide.com">http://wallpaperswide.com</a> / <a href="http://www.wallcoo.net"> www.wallcoo.net</a>
            </div>
            
          </div>
        </div>
      </div>
      </div>

  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
