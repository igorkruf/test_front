<template>
  <section>
    <section class="aside_header grid">Теги</section>
    <section class="tegi grid">
      <article v-for="(teg, index) in tegs" :key="index" class="teg">
        {{ teg }}
      </article>
    </section>
  </section>
</template>
<script>
export default {
  data() {
    return {
      tegs: [
        "fashion",
        "musik",
        "lifestyle",
        "art",
        "interior",
        "travel",
        "food",
        "health",
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.tegi {
  margin-top: $gutter;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 0.2 * $gutter;
  .teg {
    padding: 5px 15px;
    @include br(2px);
    font-family: "OpenSans-Bold";
    text-transform: uppercase;
    font-size: 12px;
    background-color: $gray_color_lighter;
  }
}
</style>