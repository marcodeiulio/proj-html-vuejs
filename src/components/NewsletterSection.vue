<template>
  <section id="newsletter">
    <div class="container section-padding">
      <div class="row justify-content-center">
        <div class="col-5">
          <description-article
            :article-classlist="newsletter.classlist"
            :article-title="newsletter.descriptionArticle.title"
            :article-heading="newsletter.descriptionArticle.heading"
            :article-paragraph="newsletter.descriptionArticle.paragraph"
          />
        </div>
        <div class="col-5">
          <div class="row gy-3">
            <div class="col-12">
              <input-field
                @input-value="userName += $event"
                :input-type="'text'"
                :input-placeholder="'Name'"
              />
            </div>
            <div class="col-12">
              <input-field
                @input-value="userEmail += $event"
                :input-type="'email'"
                :input-placeholder="'Email'"
              />
            </div>
            <div class="col-4 mt-4">
              <span @click="printForm" class="button button-solid"
                >Subscribe</span
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import DescriptionArticle from "./DescriptionArticle.vue";
import InputField from "./InputField.vue";
export default {
  name: "NewsletterSection",
  components: {
    DescriptionArticle,
    InputField,
  },
  props: {
    newsletter: Object,
  },
  data() {
    return {
      userName: "",
      userEmail: "",
    };
  },
  methods: {
    printForm() {
      console.log("User Name: " + this.userName);
      console.log("User Email: " + this.userEmail);
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

#newsletter {
  background-image: url(../assets/img/bg-1.jpg);
  background-position: center;
  background-repeat: no-repeat;
}
</style>
