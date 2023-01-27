<template>
  <div class="user-list">
    <div class="user-list__container">
      <div class="table">
        <div class="table__header">
          <span>Номер</span>
          <span>ФИО</span>
          <span>Компания</span>
          <span>Группа</span>
          <span>Присутствие</span>
        </div>
        <div class="table__body">
          <user-item
              v-for="userItem in userList"
              v-bind:userItem="userItem"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import UserItem from "@/components/UserItem";

export default {
  name: "user-list",

  components: {
    UserItem
  },

  props: {
    userList: {
      type: Array,
      required: true,
    }
  },

  data() {
    return {
      userItem: {
        id: "",
        name: "",
        company: "",
        group: "",
        status: "",
      }
    }
  },



}
</script>

<style lang="scss" scoped>
@import "@/scss/variables.scss";

.table {
  &__header {
    border-bottom: 4px solid #E9E9E9;
    padding: 0 0 7px 0;
    display: flex;
    margin: 0 0 10px 0;

    span {
      font-family: "Open Sans SemiBold", sans-serif;
      font-style: normal;
      font-weight: 600;
      font-size: 20px;
      line-height: 27px;
      color: $brown-color;
      flex: 0 1 20%;
    }
  }


}
</style>
