<template>
  <main>
    <network-section :network="descriptions.network" />
    <business-section :business="descriptions.business" />
    <process-section :process="descriptions.process" />
    <team-section :team="descriptions.team" />
    <editorial-section :editorial="descriptions.editorial" />
    <newsletter-section :newsletter="descriptions.newsletter" />
  </main>
</template>

<script>
import NetworkSection from "./NetworkSection.vue";
import BusinessSection from "./BusinessSection.vue";
import ProcessSection from "./ProcessSection.vue";
import TeamSection from "./TeamSection.vue";
import EditorialSection from "./EditorialSection.vue";
import NewsletterSection from "./NewsletterSection.vue";
export default {
  name: "MainSection",
  components: {
    NetworkSection,
    BusinessSection,
    ProcessSection,
    TeamSection,
    EditorialSection,
    NewsletterSection,
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
          descriptionArticle: {
            title: "How it works in practice",
            heading: "<span class='highlight'>Process</span> Management",
            paragraph:
              "We work with innovative methodologies to ensure that the entire reformatting process is done from start to finish as planned.",
          },
          cardArticles: [
            {
              progNumber: "01",
              heading: "Collection of information",
              headingClasslist: "",
              paragraph: "Lorem ipsum dolor sit amet consectetur.",
            },
            {
              progNumber: "02",
              heading: "Strategic planning",
              headingClasslist: "",
              paragraph: "Lorem ipsum dolor sit amet consectetur.",
            },
            {
              progNumber: "03",
              heading: "Assignment of responsibilities",
              headingClasslist: "",
              paragraph: "Lorem ipsum dolor sit amet consectetur.",
            },
            {
              progNumber: "04",
              heading: "Formatting process",
              headingClasslist: "",
              paragraph: "Lorem ipsum dolor sit amet consectetur.",
            },
            {
              progNumber: "05",
              heading: "Continuity formalization",
              headingClasslist: "",
              paragraph: "Lorem ipsum dolor sit amet consectetur.",
            },
          ],
        },
        team: {
          classlist: "article-light",
          descriptionArticle: {
            title: "We like what we do",
            heading: "<span class='highlight'>Team</span> of Experts",
            paragraph:
              "Ethics and integrity are the bases on which our professionals build their careers. They are fundamentals that become daily attitudes.",
          },
          cardArticles: [
            {
              img: "team-1.jpg",
              heading: "David Cooper",
              headingClasslist: "d-inline-block",
              paragraph: "CTO & CO-FOUNDER",
              brandIcons: true,
            },
            {
              img: "team-3.jpg",
              heading: "Oliver Jones",
              headingClasslist: "d-inline-block",
              paragraph: "CHIEF PROCUREMENT",
              brandIcons: true,
            },
            {
              img: "team-2.jpg",
              heading: "Emma Lopez",
              headingClasslist: "d-inline-block",
              paragraph: "CHIEF MARKETING",
              brandIcons: true,
            },
            {
              img: "team-4.jpg",
              heading: "T. Johnson",
              headingClasslist: "d-inline-block",
              paragraph: "CEO & PRESIDENT",
              brandIcons: true,
            },
          ],
        },
        editorial: {
          classlist: "article-dark",
          descriptionArticle: {
            title: "Our editorial content",
            heading: "Lates <span class='highlight'>News</span>",
            paragraph:
              "Every week we publish content about what is best in the business world.",
          },
          cardArticles: [
            {
              img: "news-1.jpg",
              heading: "Increasing creativity is possible for everyone",
            },
            {
              img: "news-2.jpg",
              heading: "Because market research is part of the business plan",
            },
            {
              img: "news-3.jpg",
              heading: "Working from home is now a trend",
            },
          ],
        },
        newsletter: {
          classlist: "article-light",
          descriptionArticle: {
            title: "Newsletter",
            heading: "<span class='highlight'>Know</span> First",
            paragraph:
              "Follow closely and receive content about our company and the news of the current market.",
          },
        },
      },
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
</style>
