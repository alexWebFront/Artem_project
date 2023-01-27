<template>
  <div class="page">
    <div class="page__container">
      <v-header/>
      <div class="page__content">
        <user-list v-bind:userList="userList"/>
      </div>
      <v-filter/>
    </div>
  </div>
</template>

<script>
import UserList from "@/components/UserList";
import VHeader from "@/components/VHeader";
import VFilter from "@/components/VFilter";

export default {
  components: {VFilter, VHeader, UserList},
  data() {
    return {
      userList: [
        {
          id: 1,
          name: "Зубенко Михаил Петрович",
          company: "ООО “АСОЛЬ”",
          group: "Жеромин",
          status: "",
        },
        {
          id: 2,
          name: "Зубенко Михаил Петрович",
          company: "ООО “АСОЛЬ”",
          group: "Жеромин",
          status: "",
        },
        {
          id: 3,
          name: "Зубенко Михаил Петрович",
          company: "ООО “АСОЛЬ”",
          group: "Жеромин",
          status: "",
        },
      ]
    }
  },
  methods: {}
}
</script>

<style lang="scss" scoped>

.page {
  font-family: "Open Sans Regular", sans-serif;

  &__container {
    max-width: 1920px;
    height: 100vh;
    padding: 30px 60px;
    position: relative;
  }
}
</style>
