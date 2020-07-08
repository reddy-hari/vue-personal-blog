<template>
  <div id="app">
    <app-nav></app-nav>
    <app-body-content></app-body-content>
    <app-footer></app-footer>
  </div>
</template>


<script>
// @ is an alias to /src
import BodyContent from "@/views/BodyContent.vue";
import Nav from "./components/Nav.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    appNav: Nav,
    appBodyContent: BodyContent,
    appFooter: Footer
  }
};
</script>


<style scoped>
#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
