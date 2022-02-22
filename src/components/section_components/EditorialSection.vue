<template>
  <section id="editorial">
    <div class="container section-padding">
      <div class="row">
        <div class="col-8">
          <description-article
            :article-classlist="editorial.classlist"
            :article-title="editorial.descriptionArticle.title"
            :article-heading="editorial.descriptionArticle.heading"
            :article-paragraph="editorial.descriptionArticle.paragraph"
          />
        </div>
        <div class="col-4 d-flex justify-content-end align-items-end mb-5">
          <div>
            <a href="#" class="button button-solid">See all</a>
          </div>
        </div>
      </div>
      <div class="row h-100">
        <div
          class="col-4"
          v-for="(card, index) in editorial.cardArticles"
          :key="index"
        >
          <div class="bg-card">
            <img
              :src="require(`../../assets/img/${card.img}`)"
              :alt="`thumbnail: ${card.heading}`"
            />
            <div class="dimmer">
              <card-article
                class="card-article position-relative px-5 text-center"
                :card-classlist="editorial.classlist"
                :card-heading="card.heading"
                :card-heading-classlist="card.headingClasslist"
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
  name: "EditorialSection",
  components: {
    DescriptionArticle,
    CardArticle,
  },
  props: {
    editorial: Object,
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

#editorial {
  background-color: $bg-lighter;

  .bg-card {
    display: inline-block;
    overflow: hidden;
    position: relative;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    transition: transform 0.5s;
    cursor: pointer;

    &:hover {
      transform: scale(1.05);
      transition: transform 0.5s;
    }

    img {
      pointer-events: none;
      position: absolute;
      width: 100%;
      height: 100%;
    }

    .dimmer {
      background-color: rgba(0, 0, 0, 0.438);
      position: relative;
      width: 100%;
      height: 100%;
      padding-top: 320px;
    }

    .card-article {
      color: $header-light;
    }
  }
}
</style>
