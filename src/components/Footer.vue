<template>
  <div>
    <section id="footer">
      <div class="container">

        <div class="row text-center text-xs-center text-sm-left text-md-left">

          <div class="col-xs-12 col-sm-4 col-md-4">
            <h5>Quick links</h5>
            <ul class="list-unstyled quick-links">
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>Home
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>About
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>FAQ
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>Get Started
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>Videos
                </a>
              </li>
            </ul>
          </div>
          <div class="col-xs-12 col-sm-4 col-md-4">
            <h5>Quick links</h5>
            <ul class="list-unstyled quick-links">
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>Home
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>About
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>FAQ
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>Get Started
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>Videos
                </a>
              </li>
            </ul>
          </div>
          <div class="col-xs-12 col-sm-4 col-md-4">
            <h5>Quick links</h5>
            <ul class="list-unstyled quick-links">
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>Home
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>About
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>FAQ
                </a>
              </li>
              <li>
                <a href="https://www.fiverr.com/share/qb8D02">
                  <i class="fa fa-angle-double-right"></i>Get Started
                </a>
              </li>
              <li>
                <a href="https://wwwe.sunlimetech.com" title="Design and developed by">
                  <i class="fa fa-angle-double-right"></i>Imprint
                </a>
              </li>
            </ul>
          </div>

        </div>

        <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-12 mt-2 mt-sm-5">
            <ul class="list-unstyled list-inline social text-center">
              <li class="list-inline-item">
                <a href="https://www.facebook.com/harireddy05">
                  <i class="fa fa-facebook"></i>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="https://twitter.com/harireddy05">
                  <i class="fa fa-twitter"></i>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="https://www.instagram.com/kreativemanifests/">
                  <i class="fa fa-instagram"></i>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="https://500px.com/kreativemanifests">
                  <i class="fa fa-500px"></i>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="mailto:kreativemanifests@gmail.com">
                  <i class="fa fa-envelope"></i>
                </a>
              </li>
            </ul>
          </div>
        </div>

        <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-12 mt-2 mt-sm-2 text-center text-white">
            <p>{{kmsFooterInfo}}</p>
            <p class="h6">{{rightsReserved}} | {{siteName}}</p>
          </div>
        </div>

      </div>
    </section>

  </div>
</template>

<script>
import {commonText} from '../mixins/CommonText.js';
export default {
  name: "Footer",
  mixins: [commonText],
  data() {
    return {      
      
    };
  }
};
</script>

<style scoped>
@import url("https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css");
section {
  padding: 60px 0;
}

section .section-title {
  text-align: center;
  color: #007b5e;
  margin-bottom: 50px;
  text-transform: uppercase;
}
#footer {
  background: #343A40 !important;
}
#footer h5 {
  padding-left: 10px;
  border-left: 3px solid #eeeeee;
  padding-bottom: 6px;
  margin-bottom: 20px;
  color: #ffffff;
}
#footer a {
  color: #ffffff;
  text-decoration: none !important;
  background-color: transparent;
  -webkit-text-decoration-skip: objects;
}
#footer ul.social li {
  padding: 3px 0;
}
#footer ul.social li a i {
  margin-right: 5px;
  font-size: 25px;
  -webkit-transition: 0.5s all ease;
  -moz-transition: 0.5s all ease;
  transition: 0.5s all ease;
}
#footer ul.social li:hover a i {
  font-size: 30px;
  margin-top: -10px;
}
#footer ul.social li a,
#footer ul.quick-links li a {
  color: #ffffff;
}
#footer ul.social li a:hover {
  color: #eeeeee;
}
#footer ul.quick-links li {
  padding: 3px 0;
  -webkit-transition: 0.5s all ease;
  -moz-transition: 0.5s all ease;
  transition: 0.5s all ease;
}
#footer ul.quick-links li:hover {
  padding: 3px 0;
  margin-left: 5px;
  font-weight: 700;
}
#footer ul.quick-links li a i {
  margin-right: 5px;
}
#footer ul.quick-links li:hover a i {
  font-weight: 700;
}

@media (max-width: 767px) {
  #footer h5 {
    padding-left: 0;
    border-left: transparent;
    padding-bottom: 0px;
    margin-bottom: 10px;
  }
}
</style>