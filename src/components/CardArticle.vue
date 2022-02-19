<template>
  <article :class="[cardClasslist]">
    <i :class="[cardIcon]"></i>
    <h4 :class="[cardHeadingClasslist]">{{ cardHeading }}</h4>
    <p>{{ cardParagraph }}</p>
  </article>
</template>

<script>
export default {
  name: "CardArticle",
  props: {
    cardClasslist: String,
    cardHeading: String,
    cardHeadingClasslist: String,
    cardParagraph: String,
    cardIcon: String,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
</style>
