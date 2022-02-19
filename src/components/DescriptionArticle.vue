<template>
  <article :class="[articleClasslist]">
    <h6>{{ articleTitle }}</h6>
    <h3 v-html="articleHeading"></h3>
    <p>{{ articleParagraph }}</p>
    <p v-if="articleSecondParagraph">{{ articleSecondParagraph }}</p>
  </article>
</template>

<script>
export default {
  name: "DescriptionArticle",
  props: {
    articleTitle: String,
    articleHeading: String,
    articleParagraph: String,
    articleSecondParagraph: String,
    articleClasslist: String,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
</style>
