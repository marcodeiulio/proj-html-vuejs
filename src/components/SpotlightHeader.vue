<template>
  <header>
    <section id="header-contacts" class="py-3 font-light">
      <div class="container d-flex justify-content-between align-items-center">
        <p class="m-0">Open Hours</p>
        <ul class="m-0 list-inline d-flex justify-content-around">
          <li>phone number</li>
          <li>hello@nexgen.com</li>
          <li>icon</li>
          <li>icon</li>
          <li>icon</li>
        </ul>
      </div>
    </section>
    <section id="spotlight">
      <nav id="header-nav" class="py-3">
        <ul class="nav container justify-content-end align-items-center">
          <li class="nav-item">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Services</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Process</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Team</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Blog</a>
          </li>
          <li class="nav-item">
            <a class="button button-solid" href="#" role="button"
              >Get in touch</a
            >
          </li>
        </ul>
      </nav>
      <div class="container wrapper">
        <GetInTouch />
      </div>
    </section>
  </header>
</template>

<script>
import GetInTouch from "./GetInTouch.vue";
export default {
  name: "SpotlightHeader",
  components: {
    GetInTouch,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
#header-contacts {
  color: $par-light;
  background-color: $nexgrey-dark;
  li {
    margin-right: 1.5em;
  }
}
#header-nav {
  li {
    margin-left: 30px;
  }
  a {
    color: $nexgrey-dark;
    text-transform: uppercase;
  }
}
#header-spotlight {
  height: 800px;
}

#spotlight {
  background-image: url(../assets/img/bg-6.jpg);
  background-position: center;
}
</style>
