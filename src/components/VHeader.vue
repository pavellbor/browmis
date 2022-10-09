<template>
  <header class="page-header">
    <div class="wrapper">
      <a class="logo" href="#">
        <img src="@/assets/logo.svg" />
      </a>
      <div class="nav">
        <button class="nav-btn">
          <img src="@/assets/burger.svg" />
        </button>
        <nav v-if="isNavShowed" class="nav-list">
          <a href="#">Обо мне</a>
          <a href="#">Портфолио</a>
          <a href="#">Прайс</a>
          <a href="#">Контакты</a>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isNavShowed: false,
    };
  },
};
</script>

<style lang="scss">
.page-header {
  padding-top: 20px;
  padding-bottom: 20px;
  background-color: var(--dark-color);

  .wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .nav-btn {
    background: none;
    border: none;
  }
}
</style>
