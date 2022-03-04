<template>
  <section>
    <section class="aside_header grid">Рассылка</section>
    <section class="form_rassilka_container grid">
      <section class="form_rassilka grid" ref="rassilka">
        <input
          type="text"
          v-model="email"
          class="email"
          placeholder="Ваш e-mail адрес"
          @focus="cancel_error_email"
          ref="email"
        />
        <button @click="validate_email">Подписаться</button>
      </section>
    </section>
  </section>
</template>
<script>
export default {
  data() {
    return {
      email: [],
    };
  },
  methods: {
    validate_email() {
      let regexpemail = new RegExp("[-_a-z0-9]+@[a-z]+.[a-z]{2,3}");
      // console.log(regexpemail);
      // console.log(this.email);
      if (this.email.length == 0 || !regexpemail.test(this.email)) {
        this.$refs.rassilka.classList.add("error_email");
        let vm = this;
        setTimeout(function () {
          vm.cancel_error_email();
        }, 2000);
      } else {
        this.email = [];
      }
    },
    cancel_error_email() {
      if (this.$refs.rassilka.classList.contains("error_email")) {
        this.$refs.rassilka.classList.remove("error_email");
      }
    },
  },
};
</script>
<style lang="scss" scoped>
.form_rassilka {
  position: relative;
  margin-top: $gutter;
  grid-template-columns: 1fr;
  grid-template-rows: 50px 50px;
  grid-row-gap: 0.5 * $gutter;
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
    text-transform: uppercase;
    font-size: 14px;
    font-family: "OpenSans-Bold";
    color: #fff;
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
.error_email {
  &::after {
    position: absolute;
    content: "Проверь  E-mail !";
    bottom: -30px;
    left: 10px;
    color: $gray_color;
  }
}
</style>