<template>
  <section id="team">
    <div class="container section-padding">
      <div class="row">
        <div class="col-8">
          <div class="row">
            <div class="col-10">
              <description-article
                :article-classlist="team.classlist"
                :article-title="team.descriptionArticle.title"
                :article-heading="team.descriptionArticle.heading"
                :article-paragraph="team.descriptionArticle.paragraph"
              />
            </div>
          </div>
          <div class="row">
            <div
              class="col-6 d-flex align-content-center"
              v-for="(card, index) in team.cardArticles"
              :key="index"
            >
              <figure class="me-4">
                <img
                  :src="require(`../../assets/img/${card.img}`)"
                  :alt="card.heading"
                />
              </figure>
              <div>
                <card-article
                  :card-classlist="team.classlist"
                  :card-heading="card.heading"
                  :card-heading-classlist="card.headingClasslist"
                  :card-paragraph="card.paragraph"
                  :card-icon="card.icon"
                  :brand-icons="card.brandIcons"
                />
              </div>
            </div>
          </div>
        </div>
        <div class="col-4 pe-5">
          <div class="quote mt-5 position-relative">
            <span class="quote-icon position-absolute h3">
              <i class="bi bi-quote"></i>
            </span>
            <p class="quote-title">President Speech</p>
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Libero
              aperiam dolores reiciendis perspiciatis esse.
            </p>
            <p>
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Harum ea
              iste hic voluptate.
            </p>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad ex
              ullam atque cupiditate in adipisci!
            </p>
            <p class="quote-author">T. Johnson</p>
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
  name: "TeamSection",
  components: {
    DescriptionArticle,
    CardArticle,
  },
  props: {
    team: Object,
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

#team {
  background-color: $bg-darker;

  figure {
    width: 115px;

    img {
      max-width: 100%;
      border-radius: 5px;
    }
  }

  .quote-icon {
    bottom: 5px;
    right: 25px;
    color: $highlight-dark;
  }
}
</style>
