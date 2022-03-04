<template>
  <section class="search_container grid">
    <section class="form_search grid" ref="chto_ishem">
      <input
        type="text"
        v-model="search"
        class="search"
        placeholder="Найти..."
        @focus="cancel_error_search"
        ref="chto_ishem1"
      />
      <button @click="validate_search">
        <img src="@/assets/search.svg" width="20" />
      </button>
    </section>
    <!-- <article class="chto_ishem" ref="chto_ishem">Что ищем?</article> -->
  </section>
</template>
<script>
export default {
  data() {
    return {
      search: [],
    };
  },
  methods: {
    validate_search() {
      if (this.search.length == 0) {
        this.$refs.chto_ishem.classList.add("error_search");
        let vm = this;
        setTimeout(function () {
          vm.cancel_error_search();
        }, 2000);
      } else {
        this.search = [];
      }
    },
    cancel_error_search() {
      if (this.$refs.chto_ishem.classList.contains("error_search")) {
        this.$refs.chto_ishem.classList.remove("error_search");
      }
    },
  },
};
</script>
<style lang="scss" scoped>
.form_search {
  position: relative;
  grid-template-columns: 1fr 50px;
  grid-template-rows: 50px;
  input {
    position: relative;
    border: 0px;
    @include br(0);
    width: 100%;
    height: 100%;
    background-color: $gray_color_lighter;
    outline: none;
    padding-left: 20px;
    color: $gray_color;
  }
  button {
    border: 0px;
    @include br(0);
    background-color: $accent_color;
    cursor: pointer;
    &:hover {
      opacity: 0.8;
      &:active {
        opacity: 0.9;
      }
    }
  }
}
.error_search {
  &::after {
    position: absolute;
    content: "Что ищем?";
    bottom: -30px;
    left: 10px;
    color: $gray_color;
  }
}
// .chto_ishem {
//   color: $gray_color;
//   padding: 0.5 * $gutter;
//   font-size: 14px;
//   visibility: hidden;
// }
</style>