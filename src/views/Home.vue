<template>
  <div :class="[classes.layout]">
    <div class="nav">
      <div class="nav-social">
        <div
          :class="[
            'icon',
            'flex',
            'flex-col',
            'justify-center',
            'items-center',
            classes.icon,
          ]"
        >
          <a href="#">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
              class="block w-5 h-5"
            >
              <path
                d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"
                stroke-width="1"
              />
              <path
                d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"
                stroke-width="1"
              />
            </svg>
          </a>
        </div>

        <div
          :class="[
            'icon',
            'flex',
            'flex-col',
            'justify-center',
            'items-center',
            classes.icon,
          ]"
        >
          <a href="#">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
              class="block w-5 h-5"
            >
              <path
                stroke-width="1"
                fill-rule="evenodd"
                d="M4.083 9h1.946c.089-1.546.383-2.97.837-4.118A6.004 6.004 0 004.083 9zM10 2a8 8 0 100 16 8 8 0 000-16zm0 2c-.076 0-.232.032-.465.262-.238.234-.497.623-.737 1.182-.389.907-.673 2.142-.766 3.556h3.936c-.093-1.414-.377-2.649-.766-3.556-.24-.56-.5-.948-.737-1.182C10.232 4.032 10.076 4 10 4zm3.971 5c-.089-1.546-.383-2.97-.837-4.118A6.004 6.004 0 0115.917 9h-1.946zm-2.003 2H8.032c.093 1.414.377 2.649.766 3.556.24.56.5.948.737 1.182.233.23.389.262.465.262.076 0 .232-.032.465-.262.238-.234.498-.623.737-1.182.389-.907.673-2.142.766-3.556zm1.166 4.118c.454-1.147.748-2.572.837-4.118h1.946a6.004 6.004 0 01-2.783 4.118zm-6.268 0C6.412 13.97 6.118 12.546 6.03 11H4.083a6.004 6.004 0 002.783 4.118z"
                clip-rule="evenodd"
              />
            </svg>
          </a>
        </div>
      </div>

      <div class="scroll-indicator">
        <div class="scroll-static">
          <div class="scroll-dynamic"></div>
        </div>
      </div>

      <div class="nav-projects">
        <div class="link projects">
          <a href="#PassportDo">PassportDo</a>
          <a href="#PassportDo">PassportDo</a>
        </div>
      </div>
    </div>
    <section :class="[classes.header, 'bg-black']">
      <div>
        <div class="flex p-12 md:p-24 lg:p-0">
          <div class="hidden lg:flex flex-none md:w-3/12"></div>
          <div class="flex-wrap md:flex-nowrap w-full">
            <div id="text">
              <h1
                class="header cap text-gray-100 pt-24 md:pt-64 w-full"
                v-text="$t('header.1')"
              ></h1>

              <h1
                class="header cap text-gray-100 pt-12 w-full"
                v-text="$t('header.2')"
              ></h1>
            </div>
          </div>

          <div class="hidden lg:flex flex-none md:w-3/12">
            <div class="hidden lg:flex justify-end w-full stic p-8">
              <SwitchLocale></SwitchLocale>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section :class="['container-project', 'pt-32', classes.body]">
      <div class="flex p-12 md:p-24 lg:p-0">
        <div class="hidden lg:flex flex-none w-3/12"></div>
        <div class="flex-grow">
          <div class="flex flex-wrap md:flex-nowrap gap-32">
            <div class="col-span-2 md:col-span-1 w-full md:w-8/12">
              <h1 :class="['project-title', classes.portfolio.pdo.title]">
                {{ $t("portfolio.pdo.name") }}
              </h1>

              <p :class="['project-subtitle', classes.portfolio.pdo.desc]">
                {{ $t("portfolio.pdo.desc") }}
              </p>
            </div>
            <div
              class="mt-12 md:mt-0 col-span-2 md:col-span-1 w-full md:w-4/12"
            >
              <div class="mb-6">
                <span class="eyebrow"
                  >{{ $t("portfolio.pdo.time.name") }}:</span
                >
                <span class="block description">{{
                  $t("portfolio.pdo.time.value")
                }}</span>
              </div>

              <div class="text-gray-400 mt-2">
                <span class="eyebrow">{{ $t("portfolio.pdo.use.name") }}:</span>
                <span class="block description">{{
                  $t("portfolio.pdo.use.value.0")
                }}</span>
                <span class="block description">{{
                  $t("portfolio.pdo.use.value.1")
                }}</span>
                <span class="block description">{{
                  $t("portfolio.pdo.use.value.2")
                }}</span>
              </div>
            </div>
          </div>
        </div>

        <div class="hidden lg:flex flex-none w-3/12">
          <!-- This item will not grow -->
        </div>
      </div>
    </section>

    <section :class="['container-project', 'pt-32', classes.body]">
      <img
        src="@/assets/portfolio/pdo.png"
        alt=""
        class="border-b border-gray-200"
      />
    </section>

    <section :class="['bg-white', 'pt-32', classes.body]">
      <div class="flex p-12 md:p-24 lg:p-0">
        <div class="hidden lg:flex flex-none w-3/12"></div>
        <div class="flex-grow">
          <span class="mb-2 eyebrow">
            {{ $t("portfolio.pdo.idea.name") }}
          </span>

          <h2>
            {{ $t("portfolio.pdo.idea.value") }}
          </h2>

          <div class="description">
            {{ $t("portfolio.pdo.idea.desc") }}
          </div>
        </div>

        <div class="hidden lg:flex flex-none w-3/12">
          <!-- This item will not grow -->
        </div>
      </div>
    </section>

    <section :class="['bg-white', 'pt-32', classes.body]">
      <div class="flex p-12 md:p-24 lg:p-0">
        <div class="hidden lg:flex flex-none w-3/12"></div>
        <div class="flex-grow">
          <span class="mb-2 eyebrow">
            {{ $t("portfolio.pdo.strategy.name") }}
          </span>

          <h2>
            {{ $t("portfolio.pdo.strategy.value") }}
          </h2>

          <div class="description">
            {{ $t("portfolio.pdo.strategy.desc") }}
          </div>
        </div>

        <div class="hidden lg:flex flex-none w-3/12">
          <!-- This item will not grow -->
        </div>
      </div>
    </section>

    <section :class="['bg-white', 'pt-24', classes.body]">
      <div class="flex p-12 md:p-24 lg:p-0">
        <div class="hidden lg:flex flex-none w-3/12"></div>
        <div class="flex-grow">
          <div
            class="flex flex-row flex-wrap justify-evenly md:justify-between"
          >
            <div
              class="w-1/2 lg:w-auto flex flex-col justify-start items-center mb-12 md:mb-0"
            >
              <img
                src="@/assets/portfolio/prototypes/chat.png"
                alt=""
                class="mb-3"
              />
              <p class="subinfo">{{ $t("portfolio.pdo.proto.chat") }}</p>
            </div>

            <div
              class="w-1/2 lg:w-auto flex flex-col justify-start items-center mb-12 md:mb-0"
            >
              <img
                src="@/assets/portfolio/prototypes/list.png"
                alt=""
                class="mb-3"
              />
              <p class="subinfo">{{ $t("portfolio.pdo.proto.list") }}</p>
            </div>

            <div
              class="w-1/2 lg:w-auto flex flex-col justify-start items-center mb-12 md:mb-0"
            >
              <img
                src="@/assets/portfolio/prototypes/modals.png"
                alt=""
                class="mb-3"
              />
              <p class="subinfo">{{ $t("portfolio.pdo.proto.modal") }}</p>
            </div>

            <div
              class="w-1/2 lg:w-auto flex flex-col justify-start items-center mb-12 md:mb-0"
            >
              <img
                src="@/assets/portfolio/prototypes/rating.png"
                alt=""
                class="mb-3"
              />
              <p class="subinfo">{{ $t("portfolio.pdo.proto.rating") }}</p>
            </div>
          </div>
        </div>

        <div class="hidden lg:flex flex-none w-3/12">
          <!-- This item will not grow -->
        </div>
      </div>
    </section>

    <section :class="['bg-white', 'pt-32', classes.body]">
      <div class="flex p-12 md:p-24 lg:p-0">
        <div class="hidden lg:flex flex-none w-3/12"></div>
        <div class="flex-grow">
          <span class="mb-2 eyebrow">
            {{ $t("portfolio.pdo.feature.name") }}
          </span>

          <h2>
            {{ $t("portfolio.pdo.feature.value") }}
          </h2>
        </div>

        <div class="hidden lg:flex flex-none w-3/12">
          <!-- This item will not grow -->
        </div>
      </div>
    </section>

    <section :class="['bg-white', 'pt-32', classes.body]">
      <div class="flex p-12 md:p-24 lg:p-0">
        <div class="hidden lg:flex flex-none w-3/12"></div>
        <div class="flex-grow">
          <div class="flex justify-between gap-12 md:gap-32">
            <div class="flex flex-col justify-center items-start">
              <img
                :src="$i18n.locale == 'ru' ? BannerPDO_1Ru : BannerPDO_1En"
                alt=""
                class="border-b border-gray-200"
              />
            </div>

            <div class="flex flex-col justify-center items-start">
              <img
                :src="$i18n.locale == 'ru' ? BannerPDO_2Ru : BannerPDO_2En"
                alt=""
                class="border-b border-gray-200"
              />
            </div>
          </div>
        </div>

        <div class="hidden lg:flex flex-none w-3/12">
          <!-- This item will not grow -->
        </div>
      </div>
    </section>

    <section :class="['bg-white', 'pt-32', classes.body]">
      <div class="flex p-12 md:p-24 lg:p-0">
        <div class="hidden lg:flex flex-none w-3/12"></div>
        <div class="flex-grow">
          <span class="mb-2 eyebrow">
            {{ $t("portfolio.pdo.space.name") }}
          </span>

          <h2>
            {{ $t("portfolio.pdo.space.value") }}
          </h2>
        </div>

        <div class="hidden lg:flex flex-none w-3/12">
          <!-- This item will not grow -->
        </div>
      </div>
    </section>

    <section :class="['bg-white', 'pt-32', classes.body]">
      <img
        :src="$i18n.locale == 'ru' ? PresentPDO_2Ru : PresentPDO_2En"
        alt=""
        class="border-b border-gray-200"
      />
    </section>

    <section :class="['container-project', 'pt-32', classes.body]">
      <div class="flex p-12 md:p-24 lg:p-0">
        <div class="hidden lg:flex flex-none w-3/12"></div>
        <div class="flex-grow">
          <div class="flex flex-wrap md:flex-nowrap gap-32">
            <div class="col-span-2 md:col-span-1 w-full md:w-8/12">
              <h1 :class="['project-title', classes.portfolio.event.title]">
                {{ $t("portfolio.leonica.name") }}
              </h1>

              <p :class="['project-subtitle', classes.portfolio.event.desc]">
                {{ $t("portfolio.leonica.desc") }}
              </p>
            </div>
            <div class="col-span-2 md:col-span-1 w-full md:w-4/12">
              <div class="mb-6">
                <span class="eyebrow"
                  >{{ $t("portfolio.leonica.time.name") }}:</span
                >
                <span class="block description">{{
                  $t("portfolio.leonica.time.value")
                }}</span>
              </div>

              <div class="text-gray-400 mt-2">
                <span class="eyebrow"
                  >{{ $t("portfolio.leonica.use.name") }}:</span
                >
                <span class="block description">{{
                  $t("portfolio.leonica.use.value.0")
                }}</span>
                <span class="block description">{{
                  $t("portfolio.leonica.use.value.1")
                }}</span>
                <span class="block description">{{
                  $t("portfolio.leonica.use.value.2")
                }}</span>
              </div>
            </div>
          </div>
        </div>

        <div class="hidden lg:flex flex-none w-3/12">
          <!-- This item will not grow -->
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import "@/assets/style.css";

import { Component, Vue } from "vue-property-decorator";
import HelloI18n from "@/components/HelloI18n.vue";
import SwitchLocale from "@/components/language.vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/dist/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

@Component({
  components: { HelloI18n, SwitchLocale },
})
export default class Home extends Vue {
  private BannerPDO_1Ru = require("@/assets/portfolio/banner/banner-1.png");
  private BannerPDO_1En = require("@/assets/portfolio/banner/banner-1-en.png");
  private BannerPDO_2Ru = require("@/assets/portfolio/banner/banner-2.png");
  private BannerPDO_2En = require("@/assets/portfolio/banner/banner-2-en.png");

  private PresentPDO_2Ru = require("@/assets/portfolio/pdo2.png");
  private PresentPDO_2En = require("@/assets/portfolio/pdo2-en.png");

  private classes = {
    icon: "text-gray-100",
    layout: "",
    body: "",
    header: "",
    portfolio: {
      pdo: {
        title: "",
        desc: "",
      },
      event: {
        title: "",
        desc: "",
      },
    },
  };

  mounted() {
    gsap
      .timeline({
        scrollTrigger: {
          start: 0,
          end: 0.8,
          scrub: true,
        },
      })
      .fromTo(
        "body",
        {
          scrollTrigger: {
            start: 0.5,
            trigger: "#text",
            onUpdate: (self) => {
              if (self.progress > 0.5) {
                this.classes.icon = "text-black";
                this.classes.layout = "a0-end";
                this.classes.header = "a1-end";
                this.classes.body = "a1-begin";
                this.classes.portfolio.pdo.title = "a2-begin";
                this.classes.portfolio.pdo.desc = "a3-end";
              } else {
                this.classes.icon = "text-gray-100";
                this.classes.layout = "a0-begin";
                this.classes.header = "a1-begin";
                this.classes.body = "a1-end";
                this.classes.portfolio.pdo.title = "a2-end";
                this.classes.portfolio.pdo.desc = "a3-begin";
              }
            },
          },
        },
        {}
      );
  }
}
</script>
