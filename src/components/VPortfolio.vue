<template>
  <v-section titleText="Портфолио">
    <template #content>
      <swiper
        :effect="'creative'"
        :creativeEffect="{
          prev: {
            translate: ['-50%', 0, -200],
          },
          next: {
            translate: ['50%', 0, -200],
          },
        }"
        :loopAdditionalSlides="1"
        :loop="true"
        :centeredSlides="true"
        :modules="modules"
        class="portfolio-swiper"
      >
        <swiper-slide v-for="index in 4" :key="index"
          ><img :src="getImagePath(index)"
        /></swiper-slide>
      </swiper>
    </template>
  </v-section>
</template>

<script>
import VSection from '@/layouts/VSection.vue';
import { EffectCreative } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/effect-creative';

export default {
  components: { VSection, Swiper, SwiperSlide },

  methods: {
    getImagePath(index) {
      return require(`@/assets/portfolio-${index}.jpg`);
    },
  },

  setup() {
    return {
      modules: [EffectCreative],
    };
  },
};
</script>

<style lang="scss">
.portfolio-swiper {
  margin-left: -15px;
  margin-right: -15px;
  padding-left: 15px;
  padding-right: 15px;

  .swiper-slide {
    text-align: center;
  }

  .swiper-slide:not(.swiper-slide-visible.swiper-slide-active) img {
    filter: blur(2px);
  }
}
</style>
