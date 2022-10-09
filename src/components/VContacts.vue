<template>
  <v-section titleText="Контакты">
    <template #content>
      <form class="contacts">
        <div class="row">
          <label for="name">Имя</label>
          <FormKit v-model="name" id="name" type="text" />
        </div>
        <div class="row">
          <label for="service">Услуга</label>
          <FormKit v-model="service" :options="services" id="service" type="select" />
        </div>
        <div class="row">
          <label for="phone">Телефон</label>
          <FormKit id="phone" type="tel" />
        </div>
        <div class="row">
          <label for="date">Дата</label>
          <FormKit id="date" type="date" />
        </div>
        <div class="row">
          <label for="time">Время</label>
          <FormKit id="time" type="time" />
        </div>
        <button class="submit">Записаться</button>
      </form>
    </template>
  </v-section>
</template>

<script>
import VSection from '@/layouts/VSection.vue';

export default {
  components: { VSection },

  data() {
    return {
      name: '',
      service: '',
      phone: '',
      services: [
        'Моделирование (пинцет/ воск)',
        'Окрашивание',
        'Счастье для бровей',
        'Оформление бровей (моделирование + окрашивание)',
        'Ламинирование бровей (лами + коррекция/ окрашивание - на выбор)',
        'Ламинирование бровей (лами + коррекция + окрашивание)',
      ],
    };
  },
};
</script>

<style lang="scss">
.contacts {
  .row {
    display: grid;
    grid-template-columns: 70px 1fr;
    align-items: center;
    gap: 10px;
    padding-bottom: 13px;
    margin-bottom: 13px;
    border-bottom: 2px solid #000000;
    overflow: hidden;

    label {
      font-size: 14px;
      color: rgba(0, 0, 0, 0.5);
    }

    input,
    select {
      padding: 0;
      width: 100%;
      border: none;
      background: none;
      outline: none;
    }
  }

  .submit {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 50px;
    margin-top: 30px;
    padding: 0;
    font: inherit;
    color: rgba(183, 183, 183, 1);
    background: var(--dark-color);
    border: 0;
  }
}
</style>
