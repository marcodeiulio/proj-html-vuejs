<template>
  <header>
    <section id="header-contacts" class="py-3 font-lighter">
      <div class="container d-flex justify-content-between align-items-center">
        <p class="m-0">
          <i class="fa-solid fa-clock"></i>
          Open Hours: Mon - Sat - 9:00 - 18:00
        </p>
        <ul
          class="
            m-0
            list-inline
            d-flex
            justify-content-around
            align-items-center
          "
        >
          <li v-html="contacts.phoneNumber"></li>
          <li v-html="contacts.email"></li>
          <li>
            <i class="fa-brands fa-facebook-f"></i>
          </li>
          <li>
            <i class="fa-brands fa-twitter"></i>
          </li>
          <li>
            <i class="fa-brands fa-linkedin-in"></i>
          </li>
        </ul>
      </div>
    </section>
    <section id="spotlight">
      <nav
        id="header-nav"
        class="py-4 font-light d-flex align-items-center container"
      >
        <nexgen-logo class="flex-shrink-0" :colorVersion="'dark'" />
        <ul class="nav container justify-content-end align-items-center">
          <li class="nav-item" v-for="(nav, index) in headerNavs" :key="index">
            <a class="nav-link" href="#">{{ nav }}</a>
          </li>
          <li class="nav-item">
            <a class="button button-solid" href="#" role="button"
              >Get in touch</a
            >
          </li>
        </ul>
      </nav>
      <div class="container wrapper">
        <get-in-touch />
      </div>
    </section>
  </header>
</template>

<script>
import GetInTouch from "./GetInTouch.vue";
import NexgenLogo from "./util_components/NexgenLogo.vue";
export default {
  name: "SpotlightHeader",
  components: {
    NexgenLogo,
    GetInTouch,
  },
  props: {
    headerNavs: Array,
    contacts: Object,
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
    p {
      margin: 200px;
    }
  }
}
#header-nav {
  li {
    margin-left: 20px;
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

  li:hover a {
    color: $nexgreen-dark;
  }
}
</style>
