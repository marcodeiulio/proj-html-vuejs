<template>
  <section id="business" class="position-relative">
    <div id="line" class="position-absolute"></div>

    <div class="container section-padding">
      <div class="row justify-content-center">
        <div class="col-8 text-center">
          <description-article
            :article-classlist="process.classlist"
            :article-title="process.descriptionArticle.title"
            :article-heading="process.descriptionArticle.heading"
            :article-paragraph="process.descriptionArticle.paragraph"
          />
        </div>
      </div>
      <div class="row justify-content-center text-center">
        <div
          class="col-2 px-2 d-flex flex-column align-items-center"
          v-for="(card, index) in process.cardArticles"
          :key="index"
        >
          <div
            id="prog-number"
            class="d-flex justify-content-center align-items-center mb-3"
          >
            {{ card.progNumber }}
          </div>
          <card-article
            :card-classlist="process.classlist"
            :card-heading="card.heading"
            :card-heading-classlist="card.headingClasslist"
            :card-paragraph="card.paragraph"
            :card-icon="card.icon"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import DescriptionArticle from "../util_components/DescriptionArticle.vue";
import CardArticle from "../util_components/CardArticle.vue";
export default {
  name: "ProcessSection",
  components: {
    DescriptionArticle,
    CardArticle,
  },
  props: {
    process: Object,
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

#line {
  height: 5px;
  background-color: $highlight-solid-light;
  top: 49%;
  left: 0;
  right: 0;
  z-index: 0;
}

#prog-number {
  padding: 10px;
  border-radius: 50%;
  width: 45px;
  height: 45px;
  font-weight: $heading-4-weight;
  font-size: $heading-5-size;
  color: $nexgreen-dark;
  background-color: $highlight-solid-light;
  position: relative;
}

section {
  background-color: $bg-lighter;
  .col-2 {
    width: 20%;
  }
}
</style>
