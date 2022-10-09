<template>
  <footer class="page-footer">
    <div class="wrapper">
      <span class="title"
        >Остались вопросы?<br />
        Задайте их в соц. сетях:</span
      >
      <ul class="list">
        <li class="item">Instagram @browmis_spb</li>
        <li class="item"><a href="#">Telegram</a></li>
        <li class="item">г. Санкт- Петербург</li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss">
.page-footer {
  padding-top: 40px;
  padding-bottom: 40px;
  background-color: var(--dark-color);

  .wrapper {
    display: grid;
    justify-content: center;
    text-align: center;
  }

  .title {
    margin-bottom: 15px;
    text-transform: uppercase;
    color: var(--light-color);
  }

  .list {
    display: grid;
    gap: 15px;
    margin: 0;
    padding: 0;
    list-style: none;
    color: var(--light-color);
  }
}
</style>
