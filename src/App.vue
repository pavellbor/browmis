<template>
  <v-header />
  <v-intro />
  <v-about />
  <v-principles />
  <v-portfolio />
  <v-price />
  <v-contacts />
  <v-footer />
</template>

<script>
import VHeader from '@/components/VHeader.vue';
import VIntro from './components/VIntro.vue';
import VAbout from './components/VAbout.vue';
import VPrinciples from './components/VPrinciples.vue';
import VPortfolio from './components/VPortfolio.vue';
import VPrice from './components/VPrice.vue';
import VContacts from './components/VContacts.vue';
import VFooter from './components/VFooter.vue';

export default {
  components: { VHeader, VIntro, VAbout, VPrinciples, VPortfolio, VPrice, VContacts, VFooter },
};
</script>

<style>
:root {
  --light-color: #ffffff;
  --dark-color: #575555;
}

body {
  margin: 0;
  padding: 0;
  font-family: 'Cormorant Infant', serif;
  font-size: 16px;
}

a {
  color: inherit;
  text-decoration: none;
}

.wrapper {
  padding-left: 15px;
  padding-right: 15px;
}
</style>
