<template>
  <div class="filter"> Фильтровать по:
    <div class="filter__value">Отсутствующим</div>
    <div class="filter__value">Присутствующим</div>
    <div class="filter__value filter__value-outline">Без фильтра</div>
  </div>
</template>

<script>
export default {
  name: "v-filter"
}
</script>

<style lang="scss" scoped>
@import "./src/scss/variables";

.filter {
  position: absolute;
  left: 60px;
  bottom: 36px;
  font-family: "Open Sans Bold", sans-serif;
  font-size: 30px;
  line-height: 41px;
  color: $brown-color;
  display: flex;
  align-items: center;
  justify-content: center;

  &__value {
    font-family: "Open Sans Regular", sans-serif;
    font-size: 25px;
    line-height: 34px;
    margin: 0 0 0 25px;
    cursor: pointer;
  }

  &__value-outline {
    background: $gray-light-color;
    border-radius: 20px;
    width: 181px;
    height: 53px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>

