<template>
  <footer>
    <section id="upper-footer">
      <div class="container section-padding">
        <div class="row">
          <div class="col-3 py-4 info-par">
            <nexgen-logo :colorVersion="'light'" class="mb-5" />
            <p class="mb-5">
              A Functional HTML Template for Corporate & Business.
            </p>
            <ul class="mb-5">
              <li class="mb-3" v-html="contacts.phoneNumber"></li>
              <li class="mb-3" v-html="contacts.email"></li>
              <li class="mb-3" v-html="contacts.address"></li>
            </ul>
            <a href="#" class="button button-transparent-dark">Get in Touch</a>
          </div>
          <div
            class="col-3 p-3"
            v-for="(nav, index) in footerNavs"
            :key="index"
          >
            <div class="footer-nav ps-5 py-5">
              <h4>{{ nav.title }}</h4>
              <ul>
                <li v-for="(li, i) in nav.listItems" :key="i" class="py-1">
                  <a href="#" class="info-par">
                    <i class="bi bi-chevron-right"></i>
                    {{ li }}</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="lower-footer">
      <div class="container">
        <div class="row p-4 info-par">
          <div class="col-6 text-center">
            <p>Enjoy the low price. We are tracking any intention of piracy.</p>
          </div>
          <div class="col-6 text-center">
            <p>
              &copy; 2020 NEXGEN is Proudly Powered by
              <a href="https://nexgen.codings.dev/" class="text-green"
                >Codings</a
              >.
            </p>
          </div>
        </div>
      </div>
    </section>
  </footer>
</template>

<script>
import NexgenLogo from "./util_components/NexgenLogo.vue";
export default {
  name: "HomeFooter",
  components: {
    NexgenLogo,
  },
  props: {
    footerNavs: Array,
    contacts: Object,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

#upper-footer {
  background-color: $nexgrey-darker;

  .footer-nav {
    background-color: $nexgrey-mid;
    border-radius: 10px;
  }

  h4 {
    color: $header-light;
  }

  ul {
    list-style-type: none;
    padding: 0;

    li:hover a {
      color: $nexgreen-light;
      transition: color 0.4s;
    }

    a {
      text-decoration: none;
      transition: color 0.4s;
    }
  }
}
#lower-footer {
  background-color: $nexgrey-darkest;

  p {
    margin: 0;
  }

  .text-green {
    text-decoration: none;
    transition: color 0.4s;

    &:hover {
      color: $nexgreen-light;
      transition: color 0.4s;
    }
  }
}
</style>
