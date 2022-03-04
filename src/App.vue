<template>
  <div class="main_grid grid">
    <header class="main_grid__header grid">
      <div class="content grid">
        <div class="header_nav grid">
          <a href="#0" class="grid"
            ><img
              class="logo_img"
              src="@/assets/noemi-logo.svg"
              alt="Логотип"
              width="100"
              height="23"
          /></a>
          <nav class="grid">
            <ul>
              <li v-for="(menu_item, index) in menu_items" :key="index">
                <a :href="menu_item.to">{{ menu_item.label }}</a>
              </li>
            </ul>
          </nav>
          <div class="gamburger_nav grid" @click="toggle_fon_dialog">
            <span class="line"></span><span class="line"></span
            ><span class="line"></span>
          </div>
        </div>
        <section class="slogan grid">
          Блог о творчестве, спорте <br />
          и образе жизни
        </section>
      </div>
    </header>
    <main class="main_grid__main grid">
      <div class="content grid">
        <section class="content_list_news">
          <list-news></list-news>
        </section>
        <aside>
          <section class="content_aside grid">
            <list-new-posts></list-new-posts>
            <search-form></search-form>
            <rassilka></rassilka>
            <tegi></tegi>
            <themes></themes>
          </section>
        </aside>
      </div>
    </main>
    <footer class="main_grid__footer grid">
      <div class="content grid">
        <section class="social_link grid">
          <article>
            <a href="#0">
              <svg viewBox="0 -47 512.00203 512" class="twitter">
                <path
                  d="m191.011719 419.042969c-22.140625 0-44.929688-1.792969-67.855469-5.386719-40.378906-6.335938-81.253906-27.457031-92.820312-33.78125l-30.335938-16.585938 32.84375-10.800781c35.902344-11.804687 57.742188-19.128906 84.777344-30.597656-27.070313-13.109375-47.933594-36.691406-57.976563-67.175781l-7.640625-23.195313 6.265625.957031c-5.941406-5.988281-10.632812-12.066406-14.269531-17.59375-12.933594-19.644531-19.78125-43.648437-18.324219-64.21875l1.4375-20.246093 12.121094 4.695312c-5.113281-9.65625-8.808594-19.96875-10.980469-30.777343-5.292968-26.359376-.863281-54.363282 12.476563-78.851563l10.558593-19.382813 14.121094 16.960938c44.660156 53.648438 101.226563 85.472656 168.363282 94.789062-2.742188-18.902343-.6875-37.144531 6.113281-53.496093 7.917969-19.039063 22.003906-35.183594 40.722656-46.691407 20.789063-12.777343 46-18.96875 70.988281-17.433593 26.511719 1.628906 50.582032 11.5625 69.699219 28.746093 9.335937-2.425781 16.214844-5.015624 25.511719-8.515624 5.59375-2.105469 11.9375-4.496094 19.875-7.230469l29.25-10.078125-19.074219 54.476562c1.257813-.105468 2.554687-.195312 3.910156-.253906l31.234375-1.414062-18.460937 25.230468c-1.058594 1.445313-1.328125 1.855469-1.703125 2.421875-1.488282 2.242188-3.339844 5.03125-28.679688 38.867188-6.34375 8.472656-9.511718 19.507812-8.921875 31.078125 2.246094 43.96875-3.148437 83.75-16.042969 118.234375-12.195312 32.625-31.09375 60.617187-56.164062 83.199219-31.023438 27.9375-70.582031 47.066406-117.582031 56.847656-23.054688 4.796875-47.8125 7.203125-73.4375 7.203125zm0 0"
                />
              </svg>
            </a>
          </article>
          <article>
            <a href="#0">
              <!-- //////////////////////////////////////////////// -->

              <svg viewBox="0 0 310.05 310.05" class="pinterest">
                <path
                  d="M245.265,31.772C223.923,11.284,194.388,0,162.101,0c-49.32,0-79.654,20.217-96.416,37.176
		c-20.658,20.9-32.504,48.651-32.504,76.139c0,34.513,14.436,61.003,38.611,70.858c1.623,0.665,3.256,1,4.857,1
		c5.1,0,9.141-3.337,10.541-8.69c0.816-3.071,2.707-10.647,3.529-13.936c1.76-6.495,0.338-9.619-3.5-14.142
		c-6.992-8.273-10.248-18.056-10.248-30.788c0-37.818,28.16-78.011,80.352-78.011c41.412,0,67.137,23.537,67.137,61.425
		c0,23.909-5.15,46.051-14.504,62.35c-6.5,11.325-17.93,24.825-35.477,24.825c-7.588,0-14.404-3.117-18.705-8.551
		c-4.063-5.137-5.402-11.773-3.768-18.689c1.846-7.814,4.363-15.965,6.799-23.845c4.443-14.392,8.643-27.985,8.643-38.83
		c0-18.55-11.404-31.014-28.375-31.014c-21.568,0-38.465,21.906-38.465,49.871c0,13.715,3.645,23.973,5.295,27.912
		c-2.717,11.512-18.865,79.953-21.928,92.859c-1.771,7.534-12.44,67.039,5.219,71.784c19.841,5.331,37.576-52.623,39.381-59.172
		c1.463-5.326,6.582-25.465,9.719-37.845c9.578,9.226,25,15.463,40.006,15.463c28.289,0,53.73-12.73,71.637-35.843
		c17.367-22.418,26.932-53.664,26.932-87.978C276.869,77.502,265.349,51.056,245.265,31.772z"
                />
              </svg>

              <!-- //////////////////////////////////////////////// -->
            </a>
          </article>
          <article>
            <a href="#0">
              <svg viewBox="0 0 96.124 96.123" class="facebook">
                <path
                  d="M72.089,0.02L59.624,0C45.62,0,36.57,9.285,36.57,23.656v10.907H24.037c-1.083,0-1.96,0.878-1.96,1.961v15.803
		c0,1.083,0.878,1.96,1.96,1.96h12.533v39.876c0,1.083,0.877,1.96,1.96,1.96h16.352c1.083,0,1.96-0.878,1.96-1.96V54.287h14.654
		c1.083,0,1.96-0.877,1.96-1.96l0.006-15.803c0-0.52-0.207-1.018-0.574-1.386c-0.367-0.368-0.867-0.575-1.387-0.575H56.842v-9.246
		c0-4.444,1.059-6.7,6.848-6.7l8.397-0.003c1.082,0,1.959-0.878,1.959-1.96V1.98C74.046,0.899,73.17,0.022,72.089,0.02z"
                />
              </svg>
            </a>
          </article>

          <article>
            <a href="#0">
              <svg viewBox="0 0 300 300" class="instagram">
                <path
                  id="XMLID_505_"
                  d="M38.52,0.012h222.978C282.682,0.012,300,17.336,300,38.52v222.978c0,21.178-17.318,38.49-38.502,38.49
		H38.52c-21.184,0-38.52-17.313-38.52-38.49V38.52C0,17.336,17.336,0.012,38.52,0.012z M218.546,33.329
		c-7.438,0-13.505,6.091-13.505,13.525v32.314c0,7.437,6.067,13.514,13.505,13.514h33.903c7.426,0,13.506-6.077,13.506-13.514
		V46.854c0-7.434-6.08-13.525-13.506-13.525H218.546z M266.084,126.868h-26.396c2.503,8.175,3.86,16.796,3.86,25.759
		c0,49.882-41.766,90.34-93.266,90.34c-51.487,0-93.254-40.458-93.254-90.34c0-8.963,1.37-17.584,3.861-25.759H33.35v126.732
		c0,6.563,5.359,11.902,11.916,11.902h208.907c6.563,0,11.911-5.339,11.911-11.902V126.868z M150.283,90.978
		c-33.26,0-60.24,26.128-60.24,58.388c0,32.227,26.98,58.375,60.24,58.375c33.278,0,60.259-26.148,60.259-58.375
		C210.542,117.105,183.561,90.978,150.283,90.978z"
                />
              </svg>
            </a>
          </article>
          <article>
            <a href="#0">
              <svg viewBox="0 0 310 310" class="twitter">
                <path
                  id="XMLID_829_"
                  d="M249.775,236.928c-1.613-0.873-3.58-0.789-5.119,0.221c-14.15,9.295-28.469,14.007-42.557,14.007
		c-7.678,0-14.285-1.725-20.236-5.297c-4.023-2.366-6.688-5.399-8.139-9.257c-1.107-2.978-2.43-10.9-2.43-31.739v-71.945h66.168
		c2.762,0,5-2.239,5-5V80.818c0-2.762-2.238-5-5-5h-66.168V5c0-2.762-2.238-5-5-5h-42.684c-2.523,0-4.652,1.881-4.961,4.386
		c-1.836,14.831-5.201,27.143-10.01,36.601c-4.744,9.381-11.141,17.526-19.018,24.216c-7.842,6.687-17.451,11.899-28.563,15.491
		c-2.064,0.667-3.463,2.589-3.463,4.758v42.466c0,2.761,2.238,5,5,5h28.168v100.237c0,14.492,1.523,25.36,4.656,33.218
		c3.158,7.955,8.83,15.496,16.863,22.418c7.922,6.801,17.568,12.104,28.67,15.758c10.971,3.618,23.73,5.452,37.922,5.452
		c12.416,0,24.141-1.269,34.85-3.772c10.73-2.514,22.779-6.91,35.811-13.065c1.75-0.826,2.865-2.587,2.865-4.521v-47.314
		C252.402,239.49,251.395,237.8,249.775,236.928z"
                />
              </svg>
            </a>
          </article>
        </section>
        <section class="copyright">Copyright © 2009-2022 City blog LLC</section>
      </div>
    </footer>
    <transition name="show_sm" @leave="toggle_fon_dialog">
      <side-menu
        v-if="sm"
        class="side_menu"
        :menu_items="menu_items"
        @close_dialog="toggle_show_sm"
      ></side-menu>
    </transition>
    <transition name="fade_fon_dialog" @enter="toggle_show_sm">
      <div class="fon_dialog" v-if="fon_dialog" @click="toggle_show_sm"></div>
    </transition>
  </div>
</template>

<script>
import ListNews from "@/components/list_news";
import ListNewPosts from "@/components/new_posts";
import SideMenu from "@/components/side_menu";
import SearchForm from "@/components/search";
import Rassilka from "@/components/rassilka";
import Tegi from "@/components/tegi.vue";
import Themes from "@/components/themes.vue";
export default {
  name: "App",
  data() {
    return {
      sm: false,
      fon_dialog: false,
      menu_items: [
        {
          to: "#0",
          label: "Главная",
        },
        {
          to: "#0",
          label: "Посты",
        },
        {
          to: "#0",
          label: "Статьи",
        },
        {
          to: "#0",
          label: "Теги",
        },
        {
          to: "#0",
          label: "Темы",
        },
        {
          to: "#0",
          label: "Контакты",
        },
      ],
    };
  },
  methods: {
    toggle_fon_dialog() {
      console.log("открытие закрытие фона");
      this.fon_dialog = !this.fon_dialog;
    },
    toggle_show_sm() {
      console.log("открытие/закрытие мобильного меню");
      this.sm = !this.sm;
    },
  },
  components: {
    ListNews,
    ListNewPosts,
    SideMenu,
    SearchForm,
    Rassilka,
    Tegi,
    Themes,
  },
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}
#app {
  font-family: "OpenSans-Regular";
  a {
    text-decoration: none;
    text-transform: uppercase;
    color: #000;
  }
}

.main_grid {
  min-height: 100vh;
  grid-template-rows: auto 1fr auto;
  grid-template-columns: 1fr;
  grid-row-gap: 1.5 * $gutter;
  .main_grid__header {
    background: url("./assets/banner-bg.jpg");
    background-size: cover;
    background-position: center;
    grid-template-columns: 1fr;
    justify-content: center;
    justify-items: center;
    position: relative;
    &::after {
      position: absolute;
      content: "";
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.4);
    }
    .content {
      position: relative;
      z-index: 1;
      color: #fff;
      grid-template-columns: 1fr;
      grid-template-rows: 100px 300px;
      .header_nav {
        grid-template-columns: 200px 1fr;
        grid-template-rows: 50px;
        justify-content: space-between;
        align-content: center;

        > a {
          position: relative;
          grid-template-columns: 1fr;
          grid-template-rows: 1fr;
          justify-self: center;
          align-self: center;
        }
        nav {
          position: relative;
          top: -10px;
          grid-area: nav;
          > ul {
            display: flex;
            column-gap: 0px;
            justify-content: flex-end;
            li {
              position: relative;
              list-style-type: none;
              a {
                // text-decoration: none;
                padding: 0px 25px;
                font-size: 12px;
                // text-transform: uppercase;
                color: #fff !important;
                &:hover {
                  &::after {
                    position: absolute;
                    content: " ";
                    margin-left: -35%;
                    left: 50%;
                    bottom: -10px;
                    width: 70%;
                    height: 3px;
                    background-color: $accent_color;
                  }
                }
              }
            }
          }
        }

        .gamburger_nav {
          display: none;
          position: relative;
          top: 4px;
          grid-area: gamburger_nav;
          width: 45px;
          height: 45px;
          grid-template-columns: auto;
          grid-template-rows: repeat(3, auto);
          grid-row-gap: 5px;
          justify-content: center;
          align-content: center;
          @include br(45px);
          .line {
            display: block;
            width: 25px;
            height: 2px;
            background-color: #fff;
          }
          &:hover {
            cursor: pointer;
            background-color: #ffffff4d;
          }
        }
        .logo_img {
          grid-area: logo;
        }
        grid-template-areas: "logo nav";
      }
      .slogan {
        font-size: 36px;
        padding: 20px;
        grid-template-columns: 1fr;
        grid-template-rows: 200px;
        justify-items: center;
        align-items: center;
        text-align: center;

        text-transform: uppercase;
        font-family: "OpenSans-Bold";
      }
    }
  }
  //Фон диалогов
  .fon_dialog {
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background-color: #000;
    opacity: 0.5;
    z-index: 9;
  }
  //Анимация появления фона
  .fade_fon_dialog-enter-active,
  .fade_fon_dialog-leave-active {
    transition: opacity 0.5s ease;
  }

  .fade_fon_dialog-enter-from,
  .fade_fon_dialog-leave-to {
    opacity: 0;
  }

  //////////////////////////////////////////////////////////////////////////////////////
  //Выезжающее меню/////////////////////////////////////////////////////////////////////////
  .side_menu {
    position: fixed;
    right: 0px;
    width: 300px;
    height: 100vh;
    background-color: #fff;
    z-index: 10;
    opacity: 1;
    overflow-y: auto;
    overflow-x: hidden;
  }
  //Анимация появление мобильного меню
  .show_sm-enter-active,
  .show_sm-leave-active {
    transition: right 0.5s ease;
  }

  .show_sm-enter-from,
  .show_sm-leave-to {
    right: -300px;
  }
  //////////////////////////////////////////////////////////////////////////////////////////
  .main_grid__main {
    grid-template-columns: 1fr;
    justify-items: center;
    .content {
      padding: 0px 20px;
      grid-template-columns: 70% 25%;
      justify-content: space-between;
      grid-gap: $gutter;
      .content_list_news {
        grid-template-columns: 1fr;
        // border: 2px solid green;
      }
      aside {
        // border: 2px solid green;
        .content_aside {
          grid-template-columns: 1fr;
          grid-row-gap: 2 * $gutter;
        }
        // grid-area: aside;
      }
    }
  }
  .main_grid__footer {
    grid-template-columns: 1fr;
    justify-items: center;
    .content {
      grid-template-columns: 300px;
      grid-template-rows: 90px auto;
      grid-row-gap: 50px;
      justify-content: center;
      justify-items: center;
      .social_link {
        grid-template-columns: repeat(5, 50px);
        align-items: center;
        justify-content: center;
        justify-items: center;
        svg {
          height: $hsi;
          width: $wsi;
        }
      }
      .copyright {
        color: $gray_color;
        font-size: 12px;
        margin-bottom: 50px;
      }
    }
  }
}
//медиа запросы
@media (max-width: 720px) {
  .header_nav {
    grid-template-columns: 200px 100px !important;
    nav {
      display: none;
    }
    .gamburger_nav {
      display: grid !important;
    }
    grid-template-areas: "logo gamburger_nav" !important;
  }
  //Разбиваем список новостей на две колонки и поверх img ставим title
  .main_grid__main {
    .content {
      grid-template-columns: 1fr !important;
      .list_news {
        .image_news {
          position: relative;
          width: 100%;
          img {
            width: 100%;
          }
        }
        grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
        grid-gap: $gutter;
        justify-content: center;
        .list_news__item {
          position: relative;
          grid-template-columns: 100%;
          grid-column-gap: $gutter;
          &:hover {
            &::after {
              opacity: 0.2;
            }
          }
          &::after {
            position: absolute;
            content: "";
            top: 0px;
            left: 0px;
            width: 100%;
            height: 100%;
            background-color: #000;
            opacity: 0.5;
          }
          .info {
            position: absolute;
            top: 0px;
            left: 0px;
            z-index: 1;

            grid-template-columns: 1fr;
            grid-template-rows: auto 1fr;
            grid-gap: 20px;

            .info_razdel {
              padding: 5px;
            }

            > :nth-child(1) {
              top: 0px;
              font-size: 12px;
            }
            > :nth-child(2) {
              width: 100%;
              padding: 5px;
              text-align: center;
              font-size: 16px;
              a {
                color: #fff !important;
                &:hover {
                  color: $gray_color_light !important;
                }
              }
            }
            > :nth-child(3) {
              display: none;
            }
            > :nth-child(4) {
              display: none;
            }
          }
        }
      }
      .tegi {
        justify-content: center;
      }
      .list_themes {
        grid-template-columns: 100%;
        justify-content: center;
        //Выравниваем по середине название тем(@/components/themes.vue)
        .theme {
          grid-template-columns: auto auto;
          justify-content: center;
        }
      }
    }
  }

  ///////////////////////////////////////////////////////////////
}

@media (min-width: 721px) and (max-width: 960px) {
  .header_nav {
    ul {
      justify-content: center !important;
    }
    grid-template-columns: 1fr !important;
    grid-template-areas:
      "logo"
      "nav" !important;
  }

  //main
  .main_grid__main {
    .content {
      grid-template-columns: 1fr !important;
      //Делаем резиновые колонки grid список новых постов(@/components/new_posts.vue)
      .list_new_posts {
        grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
        grid-column-gap: $gutter;
      }
      //Выравниваем по середине  теги(@/components/tegi.vue)
      .tegi {
        justify-content: center;
      }

      .list_themes {
        grid-template-columns: 100%;
        justify-content: center;
        //Выравниваем по середине название тем(@/components/themes.vue)
        .theme {
          grid-template-columns: auto auto;
          justify-content: center;
        }
      }
      .form_rassilka_container {
        grid-template-columns: 40%;
        justify-content: center;
      }
      .search_container {
        grid-template-columns: 40%;
        justify-content: center;
      }
    }
  }
}

// стилизация иконок соц сетей
path {
  fill: #000;
}
.pinterest:hover path {
  fill: #bd081c;
}
.tumblr:hover path {
  fill: #4267b2;
}
.twitter:hover path {
  fill: #1da1f2;
}
.facebook:hover path {
  fill: #4267b3;
}
.instagram:hover path {
  fill: #8a3ab9;
}
</style>
