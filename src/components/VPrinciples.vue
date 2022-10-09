<template>
  <v-section titleText="Принципы моей работы" titleShadowText="Принципы">
    <template #content>
      <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="15"
        :pagination="{ clickable: true }"
        class="principles-swiper"
      >
        <swiper-slide v-for="(item, index) in items" :key="index"
          >{{ index + 1 }}. {{ item }}</swiper-slide
        >
      </swiper>
    </template>
  </v-section>
</template>

<script>
import VSection from '@/layouts/VSection.vue';
import { Pagination } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';

export default {
  components: { VSection, Swiper, SwiperSlide },

  data() {
    return {
      items: [
        'Любовь к здоровым волоскам и натуральным бровям',
        'Безопасность и забота о здоровье каждого клиента',
        'Обязательная предварительная консультация перед началом работы',
      ],
    };
  },

  setup() {
    return {
      modules: [Pagination],
    };
  },
};
</script>

<style lang="scss">
.principles-swiper {
  margin-left: -15px;
  margin-right: -15px;
  padding-left: 15px;
  padding-right: 15px;

  .swiper-wrapper {
    padding-bottom: 30px;
  }

  .swiper-slide {
    display: flex;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
    height: 255px;
    padding: 50px;

    font-style: italic;
    font-family: 'DM Sans', sans-serif;
    text-align: center;
    color: var(--light-color);

    background-color: var(--dark-color);
  }

  .swiper-horizontal > .swiper-pagination-bullets,
  .swiper-pagination-bullets.swiper-pagination-horizontal,
  .swiper-pagination-custom,
  .swiper-pagination-fraction {
    bottom: 0;
  }

  .swiper-horizontal > .swiper-pagination-bullets .swiper-pagination-bullet,
  .principles-swiper
    .swiper-pagination-horizontal.swiper-pagination-bullets
    .swiper-pagination-bullet {
    width: 10px;
    height: 10px;
    margin: 0 5px;
  }

  .swiper-pagination-bullet-active {
    background-color: #000000;
  }
}
</style>
