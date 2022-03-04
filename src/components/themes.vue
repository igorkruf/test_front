<template>
  <section>
    <section class="aside_header grid">Темы</section>
    <section class="list_themes grid">
      <section v-for="(theme, index) in themes" :key="index" class="theme grid">
        {{ theme.name }}
        <article class="count_theme grid">
          {{ theme.count }}
        </article>
      </section>
    </section>
  </section>
</template>
<script>
export default {
  data() {
    return {
      themes: [
        { name: "Красота", count: 12 },
        { name: "Здоровье", count: 4 },
        { name: "Образ жизни", count: 145 },
        { name: "Музыка", count: 28 },
        { name: "Спорт", count: 62 },
        { name: "Йога", count: 8 },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.list_themes {
  margin-top: $gutter;
  grid-template-columns: 1fr;
  grid-row-gap: 15px;
  .theme {
    position: relative;
    grid-template-columns: auto 1fr;
    grid-template-rows: 30px;
    align-items: center;
    font-family: "OpenSans-Bold";
    font-size: 14px;
    &::after {
      position: absolute;
      content: "";
      left: 0px;
      bottom: -10px;
      width: 100%;
      height: 1px;
      background-color: $gray_color_light;
    }
    .count_theme {
      position: relative;
      top: -3px;
      left: 2px;
      color: $accent_color;
      font-size: 11px;
    }
  }
}
</style>