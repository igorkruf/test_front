<template>
  <section class="list_news grid">
    <article
      v-for="(new_m, index) in news"
      :key="index"
      class="list_news__item grid"
    >
      <section class="image_news">
        <img :src="new_m.img" />
      </section>

      <section class="info grid">
        <article class="info_razdel">
          <span v-for="(razdel, index) in new_m.razdel" :key="index">{{
            razdel
          }}</span>
        </article>
        <article>
          <a href="#0">{{ new_m.title }}</a>
        </article>
        <article class="grid">
          <span>{{ new_m.date }}</span
          ><span>{{ new_m.avtor }}</span>
        </article>
        <article>{{ new_m.excerpt }}</article>
      </section>
    </article>
  </section>
</template>
<script>
export default {
  data() {
    return {
      news: [
        {
          razdel: ["travel", "helth"],
          title: "10 мест, ради которых стоит проснуться на рассвете ",
          date: "10 июня 2019",
          avtor: "Неизвестный автор",
          excerpt:
            "Итак, вы в питере. Раннее утро. Лед с рек и каналов уже ушёл, запущены фонтаны города... Музеи ещё закрыты. Что посмотреть?",
          img: "/assets/news/last-post1.jpg",
        },
        {
          razdel: ["helth", "lifestyle"],
          title: "Йога для начинающих в домашних условиях ",
          date: "10 июля 2019",
          avtor: "Неизвестный автор",
          excerpt:
            "Расскажем, какие упражнения выбрать и как сделать коврик для занятий йогой из того, что можно найти в шкафу.",
          img: "/assets/news/last-post2.jpg",
        },
        {
          razdel: ["music"],
          title: "Лучшие музыкальные фестивали этого лета ",
          date: "13 июля 2019",
          avtor: "Неизвестный автор",
          excerpt:
            "Лето на носу, а с ним и музыкальные фестивали. На каком же из них вы разобьёте свою палатку? Мы составили список лучших летних фестивалей по всему миру.",
          img: "/assets/news/last-post3.jpg",
        },
        {
          razdel: ["lifestyle", "food"],
          title: "Наукоёмкий подход к кулинарии ",
          date: "18 июля 2019",
          avtor: "Неизвестный автор",
          excerpt:
            "Узнаем основы проектирования новых пищевых и около-пищевых опытов, вскроем физику, химию и микробиологию еды.",
          img: "/assets/news/last-post4.jpg",
        },
        {
          razdel: ["lifestyle", "interior", "art"],
          title: "Делаем модные принты на подушках для интерьера ",
          date: "10 июня 2019",
          avtor: "Неизвестный автор",
          excerpt:
            "Подушки для дивана целесообразнее заказать в съемных чехлах на молнии, если потребуется чистка подушек, проще снять чехлы, чем везти подушку в химчистку.",
          img: "/assets/news/last-post5.jpg",
        },
        {
          razdel: ["travel", "lifestyle"],
          title: "Как в первый раз отправиться в горы? ",
          date: "10 июня 2019",
          avtor: "Неизвестный автор",
          excerpt:
            "Для начала нужно определиться, в каком формате пройдет ваше путешествие. Это зависит от многих факторов, не только от ваших желаний и интересов.",
          img: "/assets/news/last-post6.jpg",
        },
        {
          razdel: ["lifestyle", "food"],
          title: "Наукоёмкий подход к кулинарии ",
          date: "18 июля 2019",
          avtor: "Неизвестный автор",
          excerpt:
            "Узнаем основы проектирования новых пищевых и около-пищевых опытов, вскроем физику, химию и микробиологию еды.",
          img: "/assets/news/last-post4.jpg",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.list_news {
  .image_news {
    position: relative;
    width: 100%;
    // border: 1px solid brown;
    img {
      width: 100%;
    }
  }

  grid-template-columns: 1fr;
  grid-row-gap: 1.5 * $gutter;
  .list_news__item {
    grid-template-columns: 45% 45%;
    grid-column-gap: $gutter;
    .info {
      // border: 1px solid red;
      grid-template-columns: 1fr;
      grid-template-rows: auto auto 40px 1fr;
      grid-gap: 10px;
      .info_razdel {
        display: flex;
        flex-wrap: wrap;
        // border: 1px solid red;
        span {
          margin-right: 15px;
        }
      }

      > :nth-child(1) {
        position: relative;
        top: -5px;
        font-family: "OpenSans-Bold";
        color: $accent_color;
        text-transform: uppercase;
        font-size: 14px;
        // border: 1px solid red;
      }
      > :nth-child(2) {
        padding-right: 20px;
        font-family: "OpenSans-Bold";
        color: #000;
        text-transform: uppercase;
        font-size: 20px;
        // border: 1px solid red;
      }
      > :nth-child(3) {
        grid-template-columns: auto 1fr;
        grid-gap: 15px;
        align-content: center;
        justify-items: start;
        font-family: "OpenSans-Bold";
        color: #000;
        font-size: 12px;
        // border: 1px solid red;
        :nth-child(1) {
          font-family: "OpenSans-Regular";
          color: $gray_color;
        }
      }
      > :nth-child(4) {
        padding-top: 10px;
        font-size: 15px;
        // border: 1px solid red;
      }
    }
  }
}
</style>