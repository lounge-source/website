<script setup>
import { ref, onMounted } from 'vue';

const menuData = ref([]);

onMounted(async () => {
  try {
    const response = await fetch('./data.json');
    if (response.ok) {
      menuData.value = await response.json();
    } else {
      console.error('Ошибка загрузки данных:', response.statusText);
    }
  } catch (error) {
    console.error('Ошибка загрузки данных:', error);
  }
});
</script>

<template>
  <div class="container">
    <div class="menu">
      <h1>
        <span class="menu__header">
          МЕНЮ
        </span>
      </h1>
      <div class="menu__note">*Количество представленных позиций могут отличаться</div>
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
                    <p class="content__item-price">{{ item.price }} ₽</p>
                  </div>
                  <div class="content__item-description">{{ item.description }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Контейнер с поддержкой контейнерных запросов */
.container {
  container-type: inline-size;
}

/* Базовая стилизация меню */
.menu {
  width: 100%;
  min-height: 100vh;
  background: url("src/assets/images/background.png") repeat;
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

    .two-columns {
      display: grid;
      gap: 8px;
      grid-template-columns: 1fr; /* Одна колонка по умолчанию */
    }

    .content__block-article {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .content__item {
      display: grid;
      grid-template-columns: max-content 1fr max-content;
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

    .content__item-description {
      color: #9e6850;
      margin-top: 8px;
    }
  }
}

/* Контейнерные запросы */
@container (width > 500px) {
  .two-columns {
    grid-template-columns: 1fr 1fr; /* Две колонки при ширине > 500px */
  }
}
</style>
