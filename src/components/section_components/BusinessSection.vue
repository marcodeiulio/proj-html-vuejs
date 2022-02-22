<template>
  <section id="business">
    <div class="container section-padding">
      <div class="row">
        <div class="col-8">
          <description-article
            :article-classlist="business.classlist"
            :article-title="business.descriptionArticle.title"
            :article-heading="business.descriptionArticle.heading"
            :article-paragraph="business.descriptionArticle.paragraph"
          />
        </div>
        <div class="col-4 d-flex justify-content-end align-items-end mb-5">
          <div>
            <a href="#" class="button button-solid">See all</a>
          </div>
        </div>
      </div>
      <div class="row g-5 justify-content-center">
        <div
          class="outer-card col-4"
          v-for="(card, index) in business.cardArticles"
          :key="index"
        >
          <div class="inner-card px-5 py-4 position-relative d-inli">
            <span class="arrow text-green position-absolute h3">
              <i class="bi bi-arrow-right-short"></i>
            </span>
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
import DescriptionArticle from "../util_components/DescriptionArticle.vue";
import CardArticle from "../util_components/CardArticle.vue";
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
@import "../../assets/scss/_vars.scss";

#business {
  background-color: $bg-light;

  .inner-card {
    background-color: #fff;
    border-radius: 10px;

    .arrow {
      right: 30px;
      color: #82c1c1;
      cursor: pointer;
    }
  }
}
</style>
