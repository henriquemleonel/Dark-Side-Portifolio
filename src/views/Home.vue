<template>
  <body>
    <div class="wrapper">
      <!--------------------- navbar start here ---------------------------------->
      <nav>
        <span id="brand">
          <router-link id="a" to="/">henriquemleonel <span class="dot">.</span></router-link>
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

        <div id="toggle" v-on:click="showMenu">
          <div class="span-toggle">menu <span class="dot">.</span></div>
        </div>
      </nav>

      <div class="resize" :class="{ 'active' : varShowMenu }">
        <div class="close-btn" v-on:click="showMenu">close <span class="dot">.</span></div>

        <ul id="menu">
          <li><router-link class="a-resize-menu" to="/">home</router-link> <span>.</span></li>
          <li><router-link class="a-resize-menu" to="/about">about</router-link> <span>.</span></li>
          <li><router-link class="a-resize-menu" to="/work">work</router-link> <span>.</span></li>
          <li>
            <router-link class="a-resize-menu" to="/contact">contact</router-link> <span>.</span>
          </li>
        </ul>
      </div>

      <!--------------------------------------------------- navbar ends here -->

      <!--------------------- hero section start here --------------------------->
      <div class="hero">
        <div class="header">
          <h1 class="line anim-typewriter">I make brands matter in culture</h1>
        </div>
      </div>

      <div class="scroll-down"></div>
      <!------------------------------------------------ hero section ends here -->

      <!--------------------- project section start here ----------------------->
      <div class="container-fluid">
        <br /><br /><br />

        <h6>Yeah! Touch, this is art.</h6>

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

          <div class="col-lg-5 project project4" @click="location.href='project.html'"></div>

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
                <p> Se interessou nos projetos? Eu posso te ajudar.</p>
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
                <p>Conecte-se comigo</p>
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
                <p>Say hello</p>
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

<script src="https://code.jquery.com/jquery-3.4.1.js"> </script>

<script>

// import gsap from 'gsap/all';
// import { TweenMax, Expo } from 'gsap/all';
// gsap.registerPlugin( TweenMax, Expo );

export default {
  name: "home",
  components: { },
  data() {
    return {
      varShowMenu: false,
    }
  },
  methods: {
    showMenu: function () {
      this.varShowMenu = !this.varShowMenu;
    }
  }
};
// import { TweenMax } from 'gsap';
</script>

<style lang="scss" scoped>

/* ------------------basics ----------------------- */
body {
  background: #0f0f0f !important;
}

.wrapper {
  margin: 0;
  padding: 0;
  width: 100vw;
  overflow-y: hidden !important;
  overflow-x: hidden;
  height: 100%;
  width: 100%;
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
      width: 14em;
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
  z-index: 2;
  width: 55px;
  height: 35px;
  cursor: pointer;
  float: right;
  transition: all 0.3s ease-out;
  visibility: hidden;
  opacity: 0;
  background-color: #0f0f0f;
  border: none;
}

.close-btn {
  position: absolute;
  right: 16px;
  min-width: 60px;
  font-weight: 300;
  z-index: 2;
  cursor: pointer;
  top: -2px;
  line-height: 80px;
  //font-size: 22px;
  color: #fff;
  letter-spacing: 1px;
  font-weight: 300;
}

.resize { 
  z-index: 1;
  top: 0px;
  position: fixed;
  background: #0f0f0f;
  width: 100%;
  height: 100%;
  visibility: hidden;
  opacity: 0;
  transition: all 0.8s ease-out;
}

.resize #menu {
  height: 90px;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
  display: table-cell;
  vertical-align: center;
}

.resize #menu li {
  display: block;
  text-align: center;
  padding: 20px 0;
  font-size: 25px;
  min-height: 60px;
  font-weight: normal;
  cursor: pointer;
  transition: all 0.3s ease-out;
}

.resize li:nth-child(1) {
  margin-top: 180px;
}

.a-resize-menu {
  color: #fff;
  letter-spacing: 2px;
}

.a-resize-menu:hover {
  text-decoration: none;
  color: aqua;
}

// .resize:
.active {
  visibility: visible;
  opacity: 1;
  transition: all 0.5s ease-out;
}

.dot {
    font-weight: 700;
  }

@media(max-width: 768px) {
  #a {
    color: #fff;
    transition: all 0.3s ease-out;
    // font-size: 18px;
    letter-spacing: 1px;
  }

  #toggle {
    visibility: visible;
    opacity: 1;
    margin-top: 6px;
    margin-right: 4px;
    width: 48px;
  }

  .span-toggle {
    color: #fff;
    //font-size: 22px;
    align-self: flex-end;
    letter-spacing: 0px;
    font-weight: 700;
  }

  nav #brand {
    margin-left: 24px;
  }

  .a-menu {
    font-size: 22px;
    font-weight: 300;
  }

  .resize li span {
    font-weight: bold;
  }

  nav #menu {
    display: none;
  }

}

@media(min-width: 769px) {
  .resize {
    visibility: hidden !important;
  }
}

// -------------------- hero section --------------------------
.hero { 
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.header h1 {
  font-weight: lighter;
  text-align: center;
  letter-spacing: -2px;
  line-height: 58px;
}

@media(max-width: 768px) {
  .hero {
    overflow-x: hidden;
  }
  .header h1 {
    font-size: 23px;
    letter-spacing: 0px;
  }
}

/** ---------------------- scroll down animation   ---------------------- */
.scroll-down {
  position: absolute;
  left: 50%;
  bottom: 100px;
  display: block;
  text-align: center;
  font-size: 20px;
  z-index: 0;
  text-decoration: none;
  text-shadow: 0;
  width: 13px;
  height: 13px;
  border-bottom: 2px solid #fff;
  border-right: 2px solid #fff;
  transform: translate(-50%, 0) rotate(45deg);
  animation: fade_move-down 3s cubic-bezier(0.19, 1, .22, 1) infinite;
}

@keyframes fade_move-down {
  0% {
    transform: translate(0, -20px) rotate(45deg);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    transform: translate(0, 20px) rotate(45deg);
    opacity: 0;
  }
}

/** --------------------------------- projects section --------------------------------- */
h6 {
  text-align: center;
}

.vertical {
  margin-top: 40px;
  border-left: 1px solid #fff;
  height: 80px;
  position: absolute;
  left: 50%;
}

.project { 
  height: 500px;
}

.project1 {
  background: url("../assets/images/dorso.jpg") no-repeat 50% 50%;
  background-size: cover;
}

.project1::after {
  content: "timeless flow.";
  font-family: "Roboto Mono";
  font-size: 36px;
  position: relative;
  color: #fff;
  display: block;
  top: 8%;
  left: -70px;
  right: 0;
  bottom: 0;
}

.project2 {
  background: url("../assets/images/woman.jpg") no-repeat 50% 50%;
  background-size: cover;
}

.project2::after {
  content: "foretime";
  font-family: "Roboto Mono";
  font-size: 36px;
  position: relative;
  color: #fff;
  display: block;
  top: 80%;
  left: 90%;
  right: 0;
  bottom: 0;
}

.project3 {
  background: url("../assets/images/man&woman.jpg") no-repeat 50% 50%;
  background-size: cover;
}

.project3::after {
  content: "never time";
  font-family: "Roboto Mono";
  font-size: 36px;
  position: relative;
  color: #fff;
  display: block;
  top: 80%;
  left: -110px;
  right: 0;
  bottom: 0;
}

.project4 {
  background: url("../assets/images/sculpture04.jpg") no-repeat 50% 50%;
  background-size: cover;
}

.project4::after {
  content: "this is the end";
  font-family: "Roboto Mono";
  font-size: 36px;
  position: relative;
  color: #fff;
  display: block;
  top: 80%;
  left: -110px;
  right: 0;
  bottom: 0;
}

@media (max-width: 768px) {
  .project {
    width: 90% !important;
    margin: 14px auto;
  }

  .vertical { display: none }

  .project1::after, .project2::after, .project3::after, .project4::after {
    display: none;
  }
}

/**-------------------------------- footer section ------------------------ */
.collab {
  text-align: right;
}

.collab p {
  font-weight: lighter !important;
  margin-bottom: 20px;
}

.hr {
  background: rgba(255, 255, 255, 0.2);
  height: 1px;
}

.info h4 {
  font-size: 18px;
  font-weight: lighter;
}

.info p {
  color: grey;
  font-weight: lighter;
}

.info li {
  font-weight: lighter;
  color: #fff;
  font-size: 16px;
  padding-left: 20px;
}

#fb::before {
  display: inline-block;
  content: '';
  border-radius: 100%;
  height: 4px;
  width: 4px;
  margin-right: 6px;
  background: #3b5998;
}

#ig::before {
  display: inline-block;
  content: '';
  border-radius: 100%;
  height: 4px;
  width: 4px;
  margin-right: 6px;
  background: #fcaf45;
}

#tw::before {
  display: inline-block;
  content: '';
  border-radius: 100%;
  height: 4px;
  width: 4px;
  margin-right: 6px;
  background: #55acee;
}

#yt::before {
  display: inline-block;
  content: '';
  border-radius: 100%;
  height: 4px;
  width: 4px;
  margin-right: 6px;
  background: #c4302b;
}

#media, #address {
  text-align: right;
}

#media ul {
  list-style: none;
}

#media ul li {
  display: inline-block;
}

@media(max-width: 768px) { 
  .collab, #media, #personal, #address {
    text-align: center;
  }

  .info ul {
    margin: 0 0 0 -22px;
    padding: 0;
  }
}

</style>
