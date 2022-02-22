<template>
  <h1 :class="[colorVersion]" role="button">
    <span class="highlight">N E X</span> G E N
  </h1>
</template>

<script>
export default {
  name: "NexgenLogo",
  props: {
    colorVersion: String,
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";
.light {
  color: $par-light;
}

.dark {
  color: #21333e;
}

.highlight {
  color: $nexgreen-light;
  background-color: $highlight;
  padding: 10px 0 10px 30px;
  border-radius: 25% 0% 0% 25% / 50% 0% 0% 50%;
}
</style>
