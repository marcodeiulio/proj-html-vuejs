<template>
  <section id="business">
    <div class="container section-padding">
      <description-article
        :article-classlist="business.classlist"
        :article-title="business.descriptionArticle.title"
        :article-heading="business.descriptionArticle.heading"
        :article-paragraph="business.descriptionArticle.paragraph"
      />
      <div class="row g-4 justify-content-center">
        <div
          class="outer-card col-4"
          v-for="(card, index) in business.cardArticles"
          :key="index"
        >
          <div class="inner-card p-4">
            <card-article
              :card-classlist="business.classlist"
              :card-heading="card.heading"
              :card-heading-classlist="card.headingClasslist"
              :card-paragraph="card.paragraph"
              :card-icon="card.icon"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import DescriptionArticle from "./DescriptionArticle.vue";
import CardArticle from "./CardArticle.vue";
export default {
  name: "BusinessSection",
  components: {
    DescriptionArticle,
    CardArticle,
  },
  props: {
    business: Object,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

#business {
  background-color: $bg-light;

  .inner-card {
    background-color: #fff;
    border-radius: 10px;
  }
}
</style>
