<template>
  <v-section titleText="Обо мне">
    <template #content>
      <div class="about">
        <p>
          Я - Настя, мастер-бровист из Санкт-Петербурга. Делаю девушек счастливее и помогаю
          подчеркнуть естественную красоту бровей.
        </p>
        <p>
          С каждым клиентом работаю индивидуально и с учетом его пожеланий, а также понимания
          анатомических особенностей лица и волос, подбираю уникальную форму бровей. В первую
          очередь я за естественность, безопасность и заботу о здоровье каждого клиента.
        </p>
        <p>С радостью подберу форму бровей, подходящую именно тебе.</p>
      </div>
    </template>
  </v-section>
</template>

<script>
import VSection from '@/layouts/VSection.vue';

export default {
  components: { VSection },
};
</script>

<style>
.about {
  font-style: italic;
  font-family: 'DM Sans', sans-serif;
}
</style>
