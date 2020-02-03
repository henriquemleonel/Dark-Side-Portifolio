<template>
  <body>
    <div class="wrapper">
      <!-- navbar start here -->
      <nav>
        <span id="brand">
          <router-link id="a" to="/">rick__</router-link>
          <!-- <a href="home">rick__</a> -->
        </span>

        <ul id="menu">
          <!-- <li><a href="index.html">home <span>.</span></a></li> -->
          <li><router-link  class="a-menu" to="/">home</router-link> <span>.</span></li>
          <li><router-link  class="a-menu" to="/about">about</router-link> <span>.</span></li>
          <li><router-link  class="a-menu" to="/work">work</router-link> <span>.</span></li>
          <li>
            <router-link class="a-menu" to="/contact">contact</router-link> <span>.</span>
          </li>
        </ul>

        <div id="toggle">
          <div class="span">menu</div>
        </div>
      </nav>

      <div class="resize">
        <div class="close-btn"></div>

        <ul id="menu">
          <li><router-link class="a-resize-menu" to="/">Home</router-link> <span>.</span></li>
          <li><router-link class="a-resize-menu" to="/about">About</router-link> <span>.</span></li>
          <li><router-link class="a-resize-menu" to="/work">Work</router-link> <span>.</span></li>
          <li>
            <router-link class="a-resize-menu" to="/contact">Contact</router-link> <span>.</span>
          </li>
        </ul>
      </div>

      <!-- navbar start here -->

      <!-- hero section start here -->
      <div class="hero">
        <div class="header">
          <h1 class="line anim-typewriter">I make brands matter in culture</h1>
        </div>
      </div>

      <div class="scroll-down"></div>
      <!-- hero section ends here -->

      <!--------------------- project section start here ----------------------->
      <div class="container-fluid">
        <br /><br /><br />

        <h6>selected projects</h6>

        <div class="vertical"></div>
        <br />

        <div class="whitespace"></div>
        <div class="whitespace"></div>

        <div class="row">
          <div class="col-lg-8"></div>

          <div class="col-lg-4 project project1" @click="location.href='project.html'"></div>
        </div>

        <div class="whitespace"></div>

        <div class="row">
          <div class="col-lg-6 project project2" @click="location.href='project.html'"></div>

          <div class="col-lg-6"></div>
        </div>

        <div class="whitespace"></div>

        <div class="row">
          <div class="col-lg-7"></div>

          <div class="col-lg-4 project project3" @click="location.href='project.html'"></div>

          <div class="col-lg-1"></div>
        </div>

        <div class="whitespace"></div>

        <div class="row">
          <div class="col-lg-1"></div>

          <div class="col-lg-5 project project5" @click="location.href='project.html'"></div>

          <div class="col-lg-6"></div>
        </div>

        <div class="whitespace"></div>

      </div>
      <!-- project section ends here ---------------------------------------->

      <!--------------------- footer starts here ------------------------------>
      <div class="footer">
        <div class="container">
          <br><br>

          <div class="collab">
            <div class="row">
              <div class='col-lg-12'>
                <p>Got a interesting project? I can help you.</p>
              </div>
            </div>
          </div>

          <br>

          <div class="hr">
            <div class="row"></div>
          </div>

          <br><br>

          <div class="info">
            <div class="row">
              <div class="col-lg-4" id="personal">
                <p>connect with me</p>
                <h4>ig @henriquemleonel</h4>
                <br><br>
              </div>

              <div class="col-lg-4" id="media">
                <p>follow me</p>
                
                <ul>
                  <li id="fb">fb</li>
                  <li id="ig">ig</li>
                  <li id="tw">tw</li>
                  <li id="yt">yt</li>
                </ul>

                <br><br>
              </div>

              <div class="col-lg-4" id="address">
                <p>say hello</p>
                <h4>henriquemleonel@outlook.com</h4>
                <br><br>
              </div>

            </div>
          </div>
        </div>
      </div>
      <!--------------------- footer ends here --------------------------------->

      <br><br><br><br>

    </div>

  </body>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  components: { }
};

// import { TweenMax } from 'gsap';
</script>

<style lang="scss" scoped>

/* ------------------basics ----------------------- */
body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  font-family: "Roboto Mono" !important;
  background: #0f0f0f !important;
  color: #fff !important;
}

.whitespace {
  width: 100%;
  height: 100px;
}

@media (max-width: 768px) {
  .whitespace {
    display: none;
  }
}

/* ----------------- tipewrite effect ---------------*/
.line {
  width: 24em;
  top: 50%;
  margin: auto;
  border-right: 2px solid rgba(255, 255, 255, 0.75);
  text-align: center;
  white-space: nowrap;
  overflow: hidden;
  transform: translateY(-50%);
}

.anim-typewriter {
  animation: typewriter 4s steps(40) 1s 1 normal both,
  blinkTextCursor 500ms steps(40) infinite normal;
}

@keyframes typewriter {
  from {
    width: 0;
  }
  to {
    width: 18em;
  }
}

@media(max-width: 768px) {
  @keyframes typewriter {
    from {
      width: 0;
    }
    to {
      width: 17em;
    }
  }
}

@keyframes blinkTextCursor {
  from {
    border-right-color: rgba(255, 255, 255, 0.75);
  }
  to {
    border-right-color: transparent;
  }
}

/** --------------------------- navigation ----------------------------- */

nav {
  width: 100%;
  background: #0f0f0f;
  height: 96px; //80px
  position: fixed;
  z-index: 1;
}

nav #brand {
  float: left;
  display: block;
  margin-left: 82px;
  line-height: 80px;
  font-weight: bold;
}

#a {
  color: #fff;
  transition: all 0.3s ease-out;
}

.a:hover {
  text-decoration: none;
}

nav #menu {
  float: left;
  right: 80px;
  position: fixed;
}

nav #menu li {
  padding-left: 40px;
  display: inline-block;
  cursor: pointer;
  font-weight: 300;
  line-height: 80px;
  position: relative;
  transition: all 0.3s ease-out;
}

nav #menu li span {
  font-weight: 700;
}

.a-menu {
  color: #fff;
}

.a-menu:hover {
  text-decoration: none;
}

#toggle {
  position: absolute;
  right: 30px;
  top: 20px;
  font-weight: 300;
  z-index: 2;
  width: 30px;
  height: 30px;
  cursor: pointer;
  float: right;
  transition: all 0.3s ease-out;
  visibility: hidden;
  opacity: 0;
}

.close-btn {
  position: absolute;
  right: 16px;
  font-weight: 300;
  z-index: 2;
  cursor: pointer;
  top: -2px;
  line-height: 80px;
}

#resize { 
  z-index: 1;
  top: 0px;
  position: fixed;
  background: #0f0f0f;
  width: 100%;
  height: 100%;
  visibility: hidden;
  opacity: 0;
  transition: all 1s ease-out;
}

#resize #menu {
  height: 90px;
  position: absolute;
  left: 45%;
  transform: translateX(-40%);
  text-align: center;
  display: table-cell;
  vertical-align: center;
}

#resize #menu li {
  display: block;
  text-align: center;
  padding: 10px 0;
  font-size: 50px;
  min-height: 50px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease-out;
}

#resize li:nth-child(1) {
  margin-top: 140px;
}

.a-resize-menu {
  color: #fff;
}

</style>
