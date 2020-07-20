<template>
  <div>
    <div style="text-align: center; padding-top: 20px;">
      <h2>
        Welcome to
        <span class="title-style">{{siteName}}</span>
        Studios
      </h2>
      <p class="subtitle-style">{{siteMoto}}</p>
    </div>

    <!-- The App Section -->
    <div class="container" style="padding: 5">
      <div class="row">
        <div class="column-66">
          <h1 class="xlarge-font">
            <b>The App</b>
          </h1>
          <h1 class="large-font" style="color:MediumSeaGreen;">
            <b>Why buy it?</b>
          </h1>
          <p>
            <span style="font-size:36px">Take photos like a pro.</span> You should buy this app because lorem ipsum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
          </p>
          <button class="button">Download Application</button>
        </div>
        <div class="column-33">
          <img src="../assets/logo.png" width="335" height="471" />
        </div>
      </div>
    </div>

    <!-- Blog Intro Section -->
    <div>
      <div class="container" style="padding: 0">
        <div class="row container">
          <div class="column-33">
            <img src="../assets/mics-img.png" alt="App" width="335" height="471" />
          </div>
          <div class="column-66">
            <h1 class="large-font">
              <b>Opinions</b>
            </h1>
            <h2 class="medium-font" style="color:#007b5e">
              <b>The Column</b>
            </h2>
            <p style="padding-left: 15px; padding-right: 15px">
              <span style="font-size:20px">When Graffiti manifests,</span>
              {{blogIntro}}
            </p>
            <router-link to="/blog">
              <button class="button" style="background-color:#007b5e">Blog</button>
            </router-link>
          </div>
        </div>
      </div>
    </div>

    <!-- The Insta Feature Section -->
    <div class="container" style="padding: 5">
      <div class="row">
        <div class="column-66">
          <h1 class="xlarge-font">
            <b>The App</b>
          </h1>
          <h1 class="large-font" style="color:MediumSeaGreen;">
            <b>Why buy it?</b>
          </h1>
          <p>
            <span style="font-size:36px">Take photos like a pro.</span> You should buy this app because lorem ipsum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
          </p>
          <button class="button">Download Application</button>
        </div>
        <div class="column-33">
          <InstaFeature/>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import { commonText } from "../mixins/CommonText";
import InstaFeature from "../embeds/InstaFeature";
export default {
  name: "Home",
  mixins: [commonText],
  components: {
    InstaFeature
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
  background-color: #007b5e;
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