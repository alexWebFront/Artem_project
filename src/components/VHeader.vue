<template>
  <div class="header">
    <div class="header__logo">
      <img src="../assets/images/logo.svg" alt="logo">
    </div>
    <div class="header__container">
      <v-input
          v-model="searchValues.searchName"
          placeholder="Поиск по имени"
      />
      <v-input
          v-model="searchValues.searchCompany"
          placeholder="Поиск по компании"
      />
      <v-button
          @click="addUser"
          class="btn-success">Добавить
      </v-button>

      <v-popup @create="closePopup" :show="this.show"/>

    </div>
    <div class="visitors">Посетители
      <div class="visitors__count">
        <span class="green">280</span> / <span class="red">35</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "v-header",
  components: {},

  data() {
    return {
      show: false,
      searchValues: {
        searchName: '',
        searchCompany: '',
      },
    }
  },
  methods: {
    addUser() {
      this.show = true;
    },
    closePopup() {
      this.show = false;
    }
  }
}

</script>

<style lang="scss" scoped>
@import "@/scss/variables.scss";

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;

  &__container {
    display: flex;
    gap: 30px;
  }
}


.visitors {
  font-family: "Open Sans Bold", sans-serif;
  font-size: 30px;
  line-height: 41px;
  color: $brown-color;

  &__count {
    text-align: right;

    .green {
      color: $green-light-color;
    }

    .red {
      color: $red-color;
    }

  }
}

</style>
