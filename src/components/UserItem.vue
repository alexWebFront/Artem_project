<template>
  <div class="user-item">
    <span class="user-item__id">{{userItem.id}}</span>
    <span class="user-item__name">{{userItem.name}}</span>
    <span class="user-item__company">{{userItem.company}}</span>
    <span class="user-item__group">{{userItem.group}}</span>
    <div class="user-item__status"></div>
  </div>
</template>

<script>
export default {
  name: "user-item",
  props: {
    userItem:{
      type: Object,
      required: true,
    }
  }
}
</script>

<style lang="scss" scoped>

.user-item {
  display: flex;
  margin-bottom: 10px;

  span {
    flex: 0 1 20%;
    font-family: "Open Sans Regular", sans-serif;
    font-size: 30px;
    line-height: 41px;
    color: #000000;
  }

  &__status {
    width: 59px;
    height: 59px;
    background: #80BB00;
    border-radius: 30px;
    margin: 0 0 0 40px;
  }

  .offline {
    background: #EC5937;
  }

}
</style>
