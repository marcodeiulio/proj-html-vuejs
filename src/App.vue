<template>
  <div id="app">
    <SpotlightHeader />
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
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
