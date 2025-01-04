<script setup>

</script>

<template>
<div class="menu">
  <h1>
    <span  class="menu__header">
      МЕНЮ
    </span>
  </h1>
  <div class="menu__note">*Количество представленных позиций могут отличаться</div>

  <div class="menu__content">
    <div class="content__header">Классика</div>
    <div class="content__block">
      <div class="content__block-article">
        <div>
          <div class="content__item">
            <p class="content__item-title">Классическая чаша</p>
            <div class="content__item-dots"></div>
            <p class="content__item-price">3 500 ₽</p>
          </div>
          <div class="content__item-description">Добавка сигарных табаков WTO | Bonche | Dogma | Kraken | Satyr Brilliant</div>
        </div>
        <div>
          <div class="content__item">
            <p class="content__item-title">Классическая чаша</p>
            <div class="content__item-dots"></div>
            <p class="content__item-price">3 500 ₽</p>
          </div>
          <div class="content__item-description">Добавка сигарных табаков WTO | Bonche | Dogma | Kraken | Satyr Brilliant</div>
        </div>
      </div>
      <div>
        <div>
          <div class="content__item">
            <p class="content__item-title">Классическая чаша</p>
            <div class="content__item-dots"></div>
            <p class="content__item-price">3 500 ₽</p>
          </div>
          <div class="content__item-description">Добавка сигарных табаков WTO | Bonche | Dogma | Kraken | Satyr Brilliant</div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped>
.menu {
  width: 100%;
  height: 100vh;
  background: url("src/assets/images/background.png");
  font-family: "Roboto", serif;
  color: #d9d1c9;
  font-weight: 100;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 30px 150px;

  .menu__header {
    color: #9e6850;
    font-weight: 100;
    font-size: 44px;
    line-height: 48px;
    letter-spacing: .1em;
    text-transform: uppercase;
  }

  .menu__note {
    font-size: 12px;
    line-height: 150%;
    text-transform: uppercase;
    color: #d9d1c9;
    margin-top: 8px;
  }

  .menu__content {
    display: flex;
    flex-direction: column;
    margin-top: 100px;

    .content__header {
      font-size: 44px;
      font-weight: 100;
      line-height: 110%;
      text-transform: uppercase;
      letter-spacing: .1em;
      color: #976a53;
      margin-bottom: 60px;
    }

    .content__item {
      display: grid
    ;
      grid-template-columns: -webkit-max-content 1fr -webkit-max-content -webkit-max-content;
      grid-template-columns: max-content 1fr max-content max-content;
      width: 100%;
      align-items: start;
    }

    .content__item-title {
      font-size: 16px;
      line-height: 120%;
      letter-spacing: .32em;
    }

    .content__item-dots {
      border-bottom: 1px dashed #d9d1c9;
      margin: 0 10px;
      height: 16px;
      line-height: 150%;
    }

    .content__item-price {

    }

    .content__block {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-column-gap: 170px;
      -moz-column-gap: 170px;
      column-gap: 170px;
    }

    .content__block-article {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .content__item-description {
      color: #9e6850;
      margin-top: 8px;
    }
  }
}
</style>