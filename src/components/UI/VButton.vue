<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "v-button"
}
</script>

<style lang="scss">
@import '@/scss/variables.scss';
.btn{
  font-family: 'Roboto Regular', sans-serif;
  font-weight: 400;
  font-size: 24px;
  line-height: 28px;
  color: $white-color;
  width: 273px;
  height: 52px;
  border-radius: 10px;
  cursor: pointer;
}
</style>
