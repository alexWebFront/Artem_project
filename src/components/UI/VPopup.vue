<template>
  <div class="popup" v-if="show">
    <div class="popup__container">
      <div class="popup__content">
        <form @submit.prevent class="form" action="#">
          <div class="form__item item">
            <div class="item__title">ФИО</div>
            <v-input class="popup__input"/>
          </div>
          <div class="form__item item">
            <div class="item__title">Компания</div>
            <v-input class="popup__input"/>
          </div>
          <div class="form__item item">
            <div class="item__title">Группа</div>
            <v-input value="Выбрать" class="popup__input"/>
          </div>
          <div class="form__item item item-checkbox">
            <div class="item__title ">Присутствие</div>
            <v-input class="checkbox" type="checkbox"/>
          </div>
          <div class="form__item item">
            <div class="item__title">Организатор</div>
            <v-select  class="form__select popup__input"/>
          </div>
        </form>
        <div class="popup__buttons">
          <v-button class="btn-success">Добавить</v-button>
          <v-button @click="popupClose" class="btn-secondary">Закрыть</v-button>
        </div>
      </div>
      <div @click="popupClose" class="popup__close">
        <img src="../../assets/icons/popup-close.svg" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "v-popup",
  props: {
    show: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    popupClose() {
      this.$emit('create');
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/scss/variables.scss';

.popup {
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  display: flex;
  z-index: 10;

  &__container {
    margin: auto;
    background: white;
    border-radius: 30px;
    min-width: 1461px;
    min-height: 775px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
  }

  &__content {
    padding: 66px 0 80px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  &__close {
    position: absolute;
    top: 20px;
    right: 20px;
    cursor: pointer;
  }

  &__buttons {
    display: flex;
    gap: 45px;
  }

  &__input {
    min-width: 502px;
    font-family: "Open Sans Regular", sans-serif;
    font-size: 32px;
    line-height: 44px;
    color: #000000;
  }
}

.form {
  min-width: 775px;
  min-height: 628px;

  &__select {
    min-width: 502px;
    height: 52px;
  }

  &__item {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .item__title {
    font-family: "Open Sans SemiBold", sans-serif;
    font-size: 32px;
    line-height: 44px;
    color: #4E3000;
  }

  .item:not(:last-child) {
    margin-bottom: 69px;
  }

  .item:last-child {
    margin-bottom: 96px;
  }

  .item-checkbox{
    display: flex;
    justify-content: flex-start;
    gap: 67px;
  }

  .checkbox{
    height: 32px;
    width: 32px;
  }
}
</style>
