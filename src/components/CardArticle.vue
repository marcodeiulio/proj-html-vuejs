<template>
  <article :class="[cardClasslist]">
    <i :class="[cardIcon]"></i>
    <h4 :class="[cardHeadingClasslist]">{{ cardHeading }}</h4>
    <p>{{ cardParagraph }}</p>
    <div v-if="brandIcons" class="brand-icons">
      <span class="icon-container">
        <i class="fa-brands fa-facebook-f"></i>
      </span>
      <span class="icon-container">
        <i class="fa-brands fa-twitter"></i>
      </span>
      <span class="icon-container">
        <i class="fa-brands fa-linkedin-in"></i>
      </span>
    </div>
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
    brandIcons: Boolean,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
</style>
