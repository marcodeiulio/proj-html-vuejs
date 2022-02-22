<template>
  <div id="app">
    <spotlight-header :header-navs="headerNavs" :contacts="contacts" />
    <main-section />
    <home-footer :footer-navs="footerNavs" :contacts="contacts" />
  </div>
</template>

<script>
import SpotlightHeader from "./components/SpotlightHeader.vue";
import MainSection from "./components/MainSection.vue";
import HomeFooter from "./components/HomeFooter.vue";
export default {
  name: "App",
  components: {
    SpotlightHeader,
    MainSection,
    HomeFooter,
  },
  data() {
    return {
      contacts: {
        phoneNumber:
          '<p class="m-0"><i class="fa-solid fa-phone me-1"></i>+1 (305) 1234-5678</p>',
        email:
          '<p class="m-0"><i class="fa-solid fa-envelope me-1"></i>hello@nexgen.com</p>',
        address:
          '<p class="m-0"><i class="fa-solid fa-location-dot me-1"></i>Main Avenue, 987</p>',
      },
      headerNavs: ["home", "about", "services", "process", "team", "blog"],
      footerNavs: [
        {
          title: "About",
          listItems: [
            "The Company",
            "Institutional",
            "Social & Events",
            "Innovation",
            "Environment",
            "Technology",
          ],
        },
        {
          title: "Services",
          listItems: [
            "Audit & Assurance",
            "Financial Advisory",
            "Analytics M&A",
            "Middle Marketing",
            "Legal Consulting",
            "Regulatory Risk",
          ],
        },
        {
          title: "Support",
          listItems: [
            "Responsibility",
            "Terms of Use",
            "About Cookies",
            "Privacy Policy",
            "Accessibility",
            "Information",
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
