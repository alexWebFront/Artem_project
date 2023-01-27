<template>
  <input
      :value="modelValue"
      @input="updateInput"

      class="input"
  >
</template>

<script>
export default {
  name: "v-input",

  props: {
    modelValue: [String, Number]
  },
  methods: {
    updateInput(event) {
      this.$emit('update:modelValue', event.target.value)
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/variables.scss";
.input {
  width: 394px;
  padding: 15px 0 15px 20px;
  filter: drop-shadow(0px 1px 4px rgba(0, 0, 0, 0.161));
  font-size: 16px;
  line-height: 22px;
  color: $gray-color;
  border-radius: 10px;
}

</style>
