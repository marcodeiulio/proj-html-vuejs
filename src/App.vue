<template>
  <div id="app">
    <SpotlightHeader />
  </div>
</template>

<script>
import SpotlightHeader from "./components/SpotlightHeader.vue";
export default {
  name: "App",
  components: {
    SpotlightHeader,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
#app {
}
</style>
