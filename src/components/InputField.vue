<template>
  <input
    :type="inputType"
    class="p-3 font-light form-control"
    :placeholder="inputPlaceholder"
    v-model="model"
    @change="emitValue"
  />
</template>

<script>
export default {
  name: "InputField",
  props: {
    inputPlaceholder: String,
    inputType: String,
  },
  data() {
    return {
      model: "",
    };
  },
  methods: {
    emitValue() {
      this.$emit("input-value", this.model);
    },
  },
};
</script>

<style scoped>
input {
  border-radius: 5px;
  font-size: 18px;
  background-color: rgba(211, 211, 211, 0.781);
  border: none;
}
</style>
