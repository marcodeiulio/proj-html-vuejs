<template>
  <div id="app">
    <SpotlightHeader :headerNavs="headerNavs" />
    <MainSection />
  </div>
</template>

<script>
import SpotlightHeader from "./components/SpotlightHeader.vue";
import MainSection from "./components/MainSection.vue";
export default {
  name: "App",
  components: {
    SpotlightHeader,
    MainSection,
  },
  data() {
    return {
      headerNavs: ["home", "about", "services", "process", "team", "blog"],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
