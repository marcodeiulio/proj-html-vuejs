<template>
  <main>
    <section id="network">
      <div class="container section-padding">
        <description-article
          :article-title="descriptions.network.title"
          :article-heading="descriptions.network.heading"
          :article-paragraph="descriptions.network.paragraph"
          :article-second-paragraph="descriptions.network.secondParagraph"
          :article-classlist="descriptions.network.classlist"
        />
      </div>
    </section>
    <section id="business">
      <div class="container section-padding">
        <description-article
          :article-title="descriptions.business.title"
          :article-heading="descriptions.business.heading"
          :article-paragraph="descriptions.business.paragraph"
          :article-classlist="descriptions.business.classlist"
        />
      </div>
    </section>
  </main>
</template>

<script>
import DescriptionArticle from "./DescriptionArticle.vue";
export default {
  name: "MainSection",
  components: {
    DescriptionArticle,
  },
  data() {
    return {
      descriptions: {
        network: {
          classlist: "article-light",
          title: "About the network",
          heading: "<span class='highlight'>The</span> Company",
          paragraph:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolore, iste. Aliquam nulla distinctio ipsa dolor voluptate quam quasi blanditiis quisquam minima quos facere excepturi unde, aspernatur rerum mollitia vero debitis. Quidem dolores odio doloremque, quod natus sint blanditiis obcaecati dolor, eum, similique iusto nulla qui vitae iure sequi aperiam beatae delectus exercitationem.",
          secondParagraph:
            "Quidem dolores odio doloremque, quod natus sint blanditiis obcaecati dolor, eum, similique iusto nulla qui vitae iure sequi aperiam beatae delectus exercitationem.",
        },
        business: {
          classlist: "article-dark",
          title: "Our business areas",
          heading: "Excellence in <span class='highlight'>Services</span>",
          paragraph:
            "We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals. These are some options that you can hire.",
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
#business {
  background-color: $bg-light;
}
</style>
