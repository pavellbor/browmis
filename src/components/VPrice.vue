<template>
  <v-section titleText="Прайс" animatedTitle>
    <template #content>
      <div class="price">
        <section v-for="(section, index) in sections" :key="index" class="group">
          <h3 class="title">{{ section.title }}</h3>
          <table class="table">
            <tr v-for="(procedure, index) in section.procedures" :key="index">
              <td>{{ procedure.name }}</td>
              <td>{{ procedure.price }}</td>
            </tr>
          </table>
        </section>
      </div>
    </template>
  </v-section>
</template>

<script>
import VSection from '@/layouts/VSection.vue';

export default {
  components: { VSection },

  data() {
    return {
      sections: [
        {
          title: 'Одиночные процедуры',
          procedures: [
            {
              name: 'Моделирование (пинцет/ воск)',
              price: '600 руб.',
            },
            {
              name: 'Окрашивание',
              price: '700 руб.',
            },
            {
              name: 'Счастье для бровей',
              price: '500 руб.',
            },
          ],
        },
        {
          title: 'Комплексные процедуры',
          procedures: [
            {
              name: 'Оформление бровей (моделирование + окрашивание)',
              price: '1300 руб.',
            },
            {
              name: 'Ламинирование бровей (лами + коррекция/ окрашивание - на выбор)',
              price: '1600 руб.',
            },
            {
              name: 'Ламинирование бровей (лами + коррекция + окрашивание)',
              price: '2000 руб.',
            },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.price {
  display: grid;
  gap: 15px;

  .group {
    text-transform: uppercase;
  }

  .title {
    margin: 0 0 5px;
    font-size: 24px;
  }

  .table {
    width: 100%;
    border-collapse: separate;
    border-spacing: 0 20px;

    td {
      border-bottom: 2px solid rgba(0, 0, 0, 0.4);
    }

    td:first-child {
      padding-right: 10px;
    }

    td:last-child {
      text-align: right;
      white-space: nowrap;
      vertical-align: bottom;
    }
  }
}
</style>
