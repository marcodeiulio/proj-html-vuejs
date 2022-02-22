<template>
  <section id="network">
    <div class="container section-padding">
      <div class="row">
        <div class="col-6 px-5">
          <description-article
            :article-classlist="network.classlist"
            :article-title="network.descriptionArticle.title"
            :article-heading="network.descriptionArticle.heading"
            :article-paragraph="network.descriptionArticle.paragraph"
            :article-second-paragraph="
              network.descriptionArticle.secondParagraph
            "
          />
        </div>
        <div class="col-6">
          <div class="row pt-5 g-5">
            <div
              class="col-6"
              v-for="(card, index) in network.cardArticles"
              :key="index"
            >
              <card-article
                :card-classlist="network.classlist"
                :card-heading="card.heading"
                :card-heading-classlist="card.headingClasslist"
                :card-paragraph="card.paragraph"
                :card-icon="card.icon"
              />
            </div>
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
    network: Object,
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

section {
  background-color: $bg-darker;
}
</style>
