<template>
  <section>
    <section class="header_sm grid" @click="$emit('close_dialog')">
      <article><img src="@/assets/close.png" height="24" width="24" /></article>
    </section>
    <ul class="list_menu_item grid">
      <transition-group name="list">
        <li
          v-for="(menu_item, index) in final_menu_items"
          :key="index"
          class="menu_item"
          @click="$emit('close_dialog')"
        >
          <a :href="menu_item.to">{{ menu_item.label }}</a>
        </li>
      </transition-group>
    </ul>
  </section>
</template>
<script>
export default {
  emits: ["close_dialog"],
  props: ["menu_items"],
  data() {
    return {
      final_menu_items: [],
    };
  },
  methods() {},
  mounted() {
    this.menu_items.forEach((element, index) => {
      let id = setInterval(() => {
        this.final_menu_items.push(element);
        clearInterval(id);
      }, 200 * index);
    });
  },
};
</script>
<style lang="scss" scoped>
.list_menu_item {
  padding: 0px 20px;
  grid-template-columns: 1fr;
  grid-gap: 10px;
  align-items: center;
  .menu_item {
    width: 100%;
    position: relative;
    list-style-type: none;
    > a {
      width: 240px;
      height: 100%;
      color: $gray_color !important;
      padding: 10px;
      display: block;
      text-decoration: none;
      &::after {
        position: absolute;
        bottom: -5px;
        left: 0;
        content: "";
        width: 100%;
        height: 1px;
        background-color: $accent_color;
      }
      @include br(5px);
      &:hover {
        color: #000 !important;
        &:active {
          color: $gray_color !important;
        }
      }
    }
  }
}
//анимация появления пунктов меню
.list-enter-active,
.list-leave-active {
  transition: all 1s ease;
}
.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translatex(100px);
}
///////////////////////////////
//img - close sm ///////////
.header_sm {
  grid-template-columns: 30px;
  padding: 20px 20px;
  justify-content: end;
  align-content: center;
  justify-items: center;
  align-items: center;
  > article {
    &:hover {
      cursor: pointer;
    }
  }
}

///////////////////
</style>