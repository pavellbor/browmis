<template>
  <section class="section">
    <div class="wrapper">
      <div class="left-column">
        <div class="title-wrapper" :class="{ 'title-wrapper--animated': animatedTitle }">
          <span class="title-shadow">{{ titleShadow }}</span>
          <h2 class="title" v-show="!animatedTitle">{{ titleText }}</h2>
        </div>
        <div class="content">
          <slot name="content" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    titleText: {
      type: String,
      required: true,
    },
    titleShadowText: {
      type: String,
      required: false,
    },
    animatedTitle: {
      type: Boolean,
      required: false,
    },
  },

  computed: {
    titleShadow() {
      if (this.animatedTitle) {
        return new Array(5).fill(this.titleText).join(' ');
      }

      return this.titleShadowText || this.titleText;
    },
  },
};
</script>

<style lang="scss">
.section {
  margin-bottom: 80px;

  .title-wrapper {
    position: relative;
    min-height: 37px;
    margin: 0 0 45px;
    text-transform: uppercase;
  }

  .title-shadow {
    position: absolute;
    top: -30px;
    font-size: 50px;
    color: rgba(0, 0, 0, 0.08);
  }

  .title-wrapper--animated {
    margin-left: -15px;
    margin-right: -15px;
    overflow-x: clip;
    white-space: nowrap;

    .title-shadow {
      animation: marquee 2s linear infinite;
    }
  }

  .title {
    font-size: 30px;
    color: #000000;
  }
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(calc(-182px));
  }
}
</style>
