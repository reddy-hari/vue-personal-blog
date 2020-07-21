<template>
  <div class="n-bg">
    <nav class="navbar navbar-expand-lg">
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarTogglerDemo03"
        aria-controls="navbarTogglerDemo03"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div>
        <router-link class="nav-link" to="/">
          <img
            src="../../public/km-logo-white.svg"
            alt="km-studios-logo"
            width="25"
            height="25"
            style="padding: 3px"
          />
          <span class="title-style">{{siteTitle}}</span>
        </router-link>
      </div>

      <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
        <div class="navbar-nav mr-auto mt-2 mt-lg-0">
          <span></span>
        </div>
        <form class="form-inline my-2 my-lg-0">
          <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
            <li class="nav-item">
              <router-link class="nav-link n-link" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link n-link" to="/photo-gallery">Gallery</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link n-link" to="/blog">Blog</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link n-link" to="/about">About</router-link>
            </li>
          </ul>
        </form>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {
      siteTitle: "Kreative Manifests Studios"
    };
  }
};
</script>

<style scoped>
.title-style {
  text-decoration: none;
  padding: 10px;
  color: #CCCECF;
}
.n-bg {
  background-image: url("../assets/universe.gif");
}
.n-link{
  text-decoration: none;
  color: #CCCECF;
}
</style>