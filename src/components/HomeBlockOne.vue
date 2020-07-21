<template>
  <div class="w3-content w3-display-container bo-shadow">
    <div class="w3-display-container mySlides">
      <img src="../assets/crimson-rail.jpg" style="width:100%" />
      <div class="w3-display-middle w3-large w3-container w3-padding-16 w3-black">Travel</div>
    </div>
    <div class="w3-display-container mySlides">
      <img src="../assets/crow-silhouette.png" style="width:100%" />
      <div class="w3-display-middle w3-large w3-container w3-padding-16 w3-black">Wilderness</div>
    </div>
    <div class="w3-display-container mySlides">
      <img src="../assets/monkey-feeding.png" style="width:100%" />
      <div class="w3-display-middle w3-large w3-container w3-padding-16 w3-black">Wildlife</div>
    </div>
    <div class="w3-display-container mySlides">
      <img src="../assets/daynight-sky.png" style="width:100%" />
      <div class="w3-display-middle w3-large w3-container w3-padding-16 w3-black">Nature</div>
    </div>

    <button class="w3-button w3-display-left w3-black" @click="plusDivs(-1)">&#10094;</button>
    <button class="w3-button w3-display-right w3-black" @click="plusDivs(-1)">&#10095;</button>
  </div>
</template>

<script>
export default {
  name: "HomeBlockOne",
  data() {
    return {
      slideIndex: 1
    };
  },
  mounted() {
    this.showDivs(this.slideIndex);
  },
  methods: {
    showDivs(n) {
      var i;
      var x = document.getElementsByClassName("mySlides");
      if (n > x.length) {
        this.slideIndex = 1;
      }
      if (n < 1) {
        this.slideIndex = x.length;
      }
      for (i = 0; i < x.length; i++) {
        x[i].style.display = "none";
      }
      x[this.slideIndex - 1].style.display = "block";
    },
    plusDivs(n) {
      this.showDivs((this.slideIndex += n));
    }
  }
};
</script>

<style scoped>
@import url("https://www.w3schools.com/w3css/4/w3.css");

.mySlides {
  display: none;
}
.bo-shadow {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
</style>