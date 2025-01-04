<script setup>
import { ref } from 'vue';
import menuDataJson from '@/assets/data.json';

const menuData = ref(menuDataJson);
</script>

<template>
  <div class="container">
    <div class="menu">
      <h1>
        <span class="menu__header">
          МЕНЮ
        </span>
      </h1>

      <div class="menu__container">
        <div v-for="(section, index) in menuData.menu" :key="index" class="menu__content">
          <div class="content__header">{{ section.category }}</div>
          <div class="two-columns">
            <div v-for="(item, idx) in section.items" :key="idx" class="content__block">
              <div class="content__block-article">
                <div>
                  <div class="content__item">
                    <p class="content__item-title">{{ item.name }}</p>
                    <div class="content__item-dots"></div>
                    <p class="content__item-size">{{ item.size }} &nbsp;</p>
                    <p class="content__item-price">{{ item.price }} ₽</p>
                  </div>
                  <div class="content__item-description">{{ item.description }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="menu__note">*Количество представленных позиций могут отличаться</div>
    </div>

  </div>
</template>

<style scoped>
.container {
  container-type: inline-size;
}

.menu {
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;

  .menu__container {
    width: 100%;
  }

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
    margin-top: 40px;
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

    .content__block-article {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .content__item {
      display: grid;
      grid-template-columns: max-content 1fr 50px 50px;
      align-items: start;
    }

    .content__item-title {
      font-size: 14px;
      line-height: 120%;
      letter-spacing: .25em;
      text-transform: uppercase;
    }

    @media (min-width:768px) {
      .content__item-title {
        font-size: 16px;
        line-height: 120%;
        letter-spacing: .25em;
        text-transform: uppercase;
      }
    }

    .content__item-dots {
      border-bottom: 1px dashed #d9d1c9;
      margin: 0 10px;
      height: 16px;
      line-height: 150%;
    }

    .content__item-size, .content__item-price {
      text-align: end;
    }

    .content__item-description {
      color: #9e6850;
      margin-top: 8px;
    }

  .two-columns {
    display: grid;
    grid-template-columns: 1fr;
    grid-auto-flow: row;
    grid-column-gap: 170px;
    -moz-column-gap: 170px;
    column-gap: 170px;
  }

    @media (min-width:768px) {
      .two-columns {
        grid-template-columns: 1fr 1fr;
      }
    }
  }
}

</style>
