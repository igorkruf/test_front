<template>
  <section>
    <section class="aside_header grid">Новые посты</section>
    <section class="list_new_posts grid">
      <section
        v-for="(new_post, index) in new_posts"
        :key="index"
        class="list_new_posts_item grid"
      >
        <section class="img_new_post grid">
          <img :src="new_post.img" />
        </section>
        <section class="new_posts_item_info grid">
          <article class="new_posts_item_date">{{ new_post.date }}</article>
          <article class="new_posts_item_title">
            <a href="#0">{{ new_post.title }}</a>
          </article>
        </section>
      </section>
    </section>
  </section>
</template>
<script>
export default {
  data() {
    return {
      new_posts: [
        {
          title: "10 мест, ради которых стоит проснуться ",
          date: "10 июня 2019",
          img: "/assets/new_posts/2.jpg",
        },
        {
          title: "Йога для начинающих ",
          date: "10 июля 2019",
          img: "/assets/new_posts/151.jpg",
        },
        {
          title: "Как мы превратили классное место в балкон",
          date: "10 июля 2019",
          img: "/assets/new_posts/45.jpg",
        },
        {
          title: "Кулинарный подход к науке",
          date: "10 июля 2019",
          img: "/assets/new_posts/501.jpg",
        },
        {
          title: "Лучшие причестки для распущенных волос",
          date: "10 июля 2019",
          img: "assets/new_posts/7.jpg",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.aside_header {
  position: relative;
  grid-template-columns: 1fr;
  justify-items: center;
  font-size: 14px;
  font-family: "OpenSans-Bold";
  text-transform: uppercase;
  top: -5px;
  &::after {
    position: absolute;
    content: "";
    bottom: -10px;
    left: 50%;
    margin-left: -35px;
    height: 3px;
    width: 70px;
    background-color: $accent_color;
  }
}
.list_new_posts {
  margin-top: $gutter;
  grid-template-columns: 1fr;
  grid-row-gap: 15px;
  .list_new_posts_item {
    grid-template-columns: 70px 1fr;
    grid-column-gap: 10px;
    .img_new_post > img {
      width: 100%;
    }
    .new_posts_item_info {
      grid-template-rows: auto 1fr;
      grid-row-gap: 5px;
      align-content: start;

      .new_posts_item_date {
        line-height: 10px;
        font-family: "OpenSans-Regular";
        font-size: 12px;
        color: $gray_color;
      }
      .new_posts_item_title {
        font-family: "OpenSans-Bold";
        line-height: 16px;
        font-size: 14px;
      }
    }
  }
}
</style>