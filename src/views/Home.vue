<template>
  <div>
    <div class="site-banner">
      <div style="padding-top: 0px">
        <h2>
          Welcome to
          <span class="title-style">{{siteName}}</span>
          Studios
        </h2>
        <p class="subtitle-style">{{siteMoto}}</p>
      </div>
    </div>

    <!-- Carousel -->
    <div style="padding: 0">
      <HomeBlockOne />
    </div>

    <!-- Section Sample -->
    <!-- <div class="container">
      <div class="row">
        <div class="column-66">
          <h1 class="large-font">
            <b>Opinions</b>
          </h1>
          <h2 class="medium-font text-primary">
            <b>The Column</b>
          </h2>
          <p>
            <span style="font-size:36px">Take photos like a pro.</span> You should buy this app because lorem ipsum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
          </p>
          <button class="button">Download Application</button>
        </div>
        <div class="column-33">
          <img src="../assets/logo.png" width="335" height="471" />
        </div>
      </div>
    </div>-->

    <hr />

    <!-- Blog Intro Section -->
    <div>
      <div class="container" style="padding: 0">
        <div class="row">
          <div class="column-33">
            <img src="../assets/mics-img.png" alt="Blog-Intro" width="335" height="471" />
          </div>
          <div class="column-66" style="text-align: left">
            <h2 class="large-font" style="padding-top: 30px;">
              <b>Opinions</b> |
              <span class="medium-font text-primary">
                <b>The Column</b>
              </span>
            </h2>

            <p style="padding: 15px">
              <span style="font-size:20px">When Graffiti manifests,</span>
              {{blogIntro}}
            </p>

            <router-link to="/blog" style="padding: 15px">
              <button class="button" style="background-color: #007BFF;">Read the Blog</button>
            </router-link>
          </div>
        </div>
      </div>
    </div>

    <hr />

    <!-- The Insta Feature Section -->
    <div class="container" style="padding: 0">
      <h2 class="large-font" style="padding-top: 30px; padding-bottom: 20px;">
        <span style="color:#007BFF">
          <b>The Visuals</b>
        </span> |
        <span>
          <span>Check out my Insta!</span>
        </span>
      </h2>

      <div class="row">
        <div class="column-33">
          <InstaLohgad />
        </div>
        <div class="column-33">
          <InstaBean />
        </div>
        <div class="column-33">
          <InstaFriends />
        </div>
      </div>

    </div>
  </div>
</template>

<script>
import { commonText } from "../mixins/CommonText";
import InstaBean from "../embeds/InstaBean";
import InstaLohgad from "../embeds/InstaLohgad";
import InstaFriends from "../embeds/InstaFriends";

import HomeBlockOne from "../components/HomeBlockOne";

export default {
  name: "Home",
  mixins: [commonText],
  components: {
    InstaBean,
    InstaLohgad,
    InstaFriends,
    HomeBlockOne
  }
};
</script>

<style scoped>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.container {
  padding: 64px;
}

.row:after {
  content: "";
  display: table;
  clear: both;
}

.column-66 {
  float: left;
  width: 66.66666%;
  padding: 20px;
}

.column-33 {
  float: left;
  width: 33.33333%;
  padding: 20px;
}

.large-font {
  font-size: 48px;
}

.xlarge-font {
  font-size: 64px;
}

.button {
  border: none;
  color: white;
  padding: 14px 28px;
  font-size: 16px;
  cursor: pointer;
  background-color: #007bff;
}

img {
  display: block;
  height: auto;
  max-width: 100%;
}

.title-style {
  font-weight: bold;
}

.subtitle-style {
  font-family: "Courier New", Courier, monospace;
}

.site-banner {
  color: #9a9da0;
  text-align: center;
  height: 200px;
  padding-top: 5px;
  background-image: url("../assets/universe.gif");
}

@media screen and (max-width: 1000px) {
  .column-66,
  .column-33 {
    width: 100%;
    text-align: center;
  }
  img {
    margin: auto;
  }
}
</style>