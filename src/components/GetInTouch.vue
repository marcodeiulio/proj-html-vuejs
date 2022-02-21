<template>
  <div id="get-in-touch">
    <div class="row">
      <div class="col-6"></div>
      <div class="col-6">
        <h5>fusions & acquisitions</h5>
        <h2>Insurance Consulting</h2>
        <div class="row g-3">
          <div class="col-5">
            <input-field :input-type="'text'" :input-placeholder="'Name'" />
          </div>
          <div class="col-5">
            <input-field :input-type="'email'" :input-placeholder="'Email'" />
          </div>
          <div class="col-5">
            <input-field :input-type="'tel'" :input-placeholder="'Phone'" />
          </div>
          <div class="col-5">
            <input-field
              :input-type="'text'"
              :input-placeholder="'More Info'"
            />
          </div>
          <div class="col-10 py-2">
            <a href="#" class="button button-solid">Get in touch</a>
            <a href="#" class="button button-transparent">read more</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import InputField from "./InputField.vue";
export default {
  name: "GetInTouch",
  components: {
    InputField,
  },
};
</script>

<style scoped lang="scss">
#get-in-touch {
  display: flex;
  align-items: center;
  height: 800px;
  .col-10 {
    a {
      margin-right: 50px;
    }
  }
}
</style>
