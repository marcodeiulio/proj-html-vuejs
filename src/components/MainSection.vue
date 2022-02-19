<template>
  <main>
    <section id="network">
      <div class="container section-padding">
        <div class="row">
          <div class="col-6 px-5">
            <description-article
              :article-classlist="descriptions.network.classlist"
              :article-title="descriptions.network.descriptionArticle.title"
              :article-heading="descriptions.network.descriptionArticle.heading"
              :article-paragraph="
                descriptions.network.descriptionArticle.paragraph
              "
              :article-second-paragraph="
                descriptions.network.descriptionArticle.secondParagraph
              "
            />
          </div>
          <div class="col-6">
            <div class="row pt-5 g-5">
              <div
                class="col-6"
                v-for="(card, index) in descriptions.network.cardArticles"
                :key="index"
              >
                <card-article
                  :card-classlist="descriptions.network.classlist"
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
    <business-section :business="descriptions.business" />
  </main>
</template>

<script>
import DescriptionArticle from "./DescriptionArticle.vue";
import CardArticle from "./CardArticle.vue";
import BusinessSection from "./BusinessSection.vue";
export default {
  name: "MainSection",
  components: {
    CardArticle,
    DescriptionArticle,
    BusinessSection,
  },
  data() {
    return {
      descriptions: {
        network: {
          classlist: "article-light",
          descriptionArticle: {
            title: "About the network",
            heading: "<span class='highlight'>The</span> Company",
            paragraph:
              "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolore, iste. Aliquam nulla distinctio ipsa dolor voluptate quam quasi blanditiis quisquam minima quos facere excepturi unde, aspernatur rerum mollitia vero debitis.",
            secondParagraph:
              "Quidem dolores odio doloremque, quod natus sint blanditiis obcaecati dolor, eum, similique iusto nulla qui vitae iure sequi aperiam beatae delectus exercitationem.",
          },
          cardArticles: [
            {
              icon: "bi bi-award h4 me-2",
              heading: "Tradition",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
            {
              icon: "bi bi-file-earmark-lock h4 me-2",
              heading: "Security",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
            {
              icon: "bi bi-pencil-square h4 me-2",
              heading: "Certificate",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
            {
              icon: "bi bi-mortarboard h4 me-2",
              heading: "Expertise",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
          ],
        },
        business: {
          classlist: "article-dark",
          descriptionArticle: {
            title: "Our business areas",
            heading: "Excellence in <span class='highlight'>Services</span>",
            paragraph:
              "We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals. These are some options that you can hire.",
          },
          cardArticles: [
            {
              icon: "bi bi-diagram-2 h3 d-block",
              heading: "Audit & Assurance",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
            {
              icon: "bi bi-briefcase h3 d-block",
              heading: "Financial Advisory",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
            {
              icon: "bi bi-bar-chart h3 d-block",
              heading: "Analytics and M&A",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
            {
              icon: "bi bi-cart2 h3 d-block",
              heading: "Middle Marketing",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
            {
              icon: "bi bi-globe h3 d-block",
              heading: "Legal Consulting",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
            {
              icon: "bi bi-inbox h3 d-block",
              heading: "Regulatory Risk",
              headingClasslist: "d-inline-block",
              paragraph:
                "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
            },
          ],
        },
        process: {
          classlist: "article-dark",
          title: "How it works in practice",
          heading: "<span class='highlight'>Process</span> Management",
          paragraph:
            "We work with innovative methodologies to ensure that the entire reformatting process is done from start to finish as planned.",
        },
        team: {
          classlist: "article-light",
          title: "We like what we do",
          heading: "<span class='highlight'>Team</span> of Experts",
          paragraph:
            "Ethics and integrity are the bases on which our professionals build their careers. They are fundamentals that become daily attitudes.",
        },
        editorial: {
          classlist: "article-dark",
          title: "Our editorial content",
          heading: "Lates <span class='highlight'>News</span>",
          paragraph:
            "Every week we publish content about what is best in the business world.",
        },
        newsletter: {
          classlist: "article-light",
          title: "Newsletter",
          heading: "<span class='highlight'>Know</span> First",
          paragraph:
            "Follow closely and receive content about our company and the news of the current market.",
        },
      },
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

#network {
  background-color: $bg-darker;
}
</style>
