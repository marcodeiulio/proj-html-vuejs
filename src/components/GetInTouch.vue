<template>
  <div id="get-in-touch">
    <div class="row">
      <div class="col-6"></div>
      <div class="col-6">
        <h5>fusions & acquisitions</h5>
        <h2>Insurance Consulting</h2>
        <div class="row g-3">
          <div class="col-5">
            <input-field
              @input-value="userName += $event.trim()"
              :input-type="'text'"
              :input-placeholder="'Name'"
            />
          </div>
          <div class="col-5">
            <input-field
              @input-value="userEmail += $event.trim()"
              :input-type="'email'"
              :input-placeholder="'Email'"
            />
          </div>
          <div class="col-5">
            <input-field
              @input-value="userPhone += $event.trim()"
              :input-type="'tel'"
              :input-placeholder="'Phone'"
            />
          </div>
          <div class="col-5">
            <input-field
              @input-value="userInfo += $event.trim()"
              :input-type="'text'"
              :input-placeholder="'More Info'"
            />
          </div>
          <div class="col-10 py-2">
            <span class="button button-solid me-5" @click="printForm"
              >Get in touch</span
            >
            <a href="#" class="button button-transparent">read more</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import InputField from "./util_components/InputField.vue";
export default {
  name: "GetInTouch",
  components: {
    InputField,
  },
  data() {
    return {
      userName: "",
      userEmail: "",
      userPhone: "",
      userInfo: "",
    };
  },
  methods: {
    printForm() {
      console.log("User Name: " + this.userName);
      if (
        !this.userEmail.includes("@") ||
        !this.userEmail.includes(".") ||
        this.userEmail.includes(" ")
      )
        console.log("Invalid Email Address");
      else console.log("User Email: " + this.userEmail);
      console.log("User Phone: " + this.userPhone);
      console.log("User Info: " + this.userInfo);
      this.userName = "";
      this.userEmail = "";
      this.userPhone = "";
      this.userInfo = "";
    },
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
