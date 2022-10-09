<template>
  <section class="intro">
    <div class="wrapper">
      <h1 class="title">Брови говорят громче слов</h1>
      <p class="desc">Сделаю брови, о которых ты мечтаешь</p>
      <a class="btn" href="#">Записаться</a>
      <img class="picture" src="@/assets/master.png" />
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
.intro {
  margin-bottom: 80px;
  padding-top: 20px;
  background-color: var(--dark-color);

  .wrapper {
    display: grid;
    justify-items: center;
    text-align: center;
  }

  .title {
    margin: 0 0 30px;
    font-size: 45px;
    text-transform: uppercase;
  }

  .desc {
    margin: 0 0 30px;
    font-style: italic;
    font-family: 'DM Sans', sans-serif;
    text-transform: uppercase;
    color: #242424;
  }

  .btn {
    box-sizing: border-box;
    width: 100%;
    max-width: 375px;
    margin-bottom: 30px;
    padding: 13px;
    text-decoration: none;
    color: var(--light-color);
    border: 1px solid var(--light-color);
  }

  .picture {
    margin: 0 -15px;
  }
}
</style>
