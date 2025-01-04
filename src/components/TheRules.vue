<template>
  <div class="rules">
    <div class="rules__section rules__section--damage">
      <h3 class="rules__subtitle">Порча имущества</h3>

      <div class="rules__block">
        <div v-for="(rule) in rules" class="rules__block-article">
          <div class="rules__item">
            <p class="rules__item-title">{{ rule.name }}</p>
            <div class="rules__item-dots"></div>
            <p class="rules__item-price">{{ rule.price }}</p>
          </div>
        </div>
      </div>
    </div>

    <div class="rules__section rules__section--casual">
      <h2 class="rules__title">Правила заведения</h2>
      <p class="rules__text">В заведение допускаются лица, достигшие 18+ при предъявлении удостоверения личности.</p>
      <p class="rules__text">Запрещается приносить, доставать и употреблять психотропные и наркотические вещества в заведении.</p>
      <p class="rules__text">Мы не несём ответственности за пропавшие личные вещи и деньги.</p>
      <p class="rules__text">Гости заведения обязаны соблюдать правила общественного порядка.</p>
      <p class="rules__text">В случае сильного алкогольного или наркотического опьянения вам может быть отказано в посещении и обслуживании, а также по иным обстоятельствам без объяснения причин.</p>
    </div>

    <div class="rules__section rules__section--corkage">
      <p class="rules__text">*Пробковый сбор: <span class="rules__highlight">250 ₽</span></p>
      <p class="rules__text">**Питьевые и безалкогольные напитки приносить запрещено.</p>
    </div>
  </div>
</template>

<script setup>
const rules = [
  {
    name: 'Бой посуды',
    price: 'от 200 до 1500 ₽'
  },
  {
    name: 'Диван',
    price: 'от 5000 до 15000 ₽'
  },
  {
    name: 'Кресло',
    price: 'от 8000 до 10000 ₽'
  },
    {
    name: 'PS4, PS5',
    price: 'от 8000 до 70000 ₽'
  },
  {
    name: 'Джойстики',
    price: '8000 ₽'
  },
  {
    name: 'Телевизор',
    price: 'от 30000 до 55000 ₽'
  },
  {
    name: 'Чаша',
    price: 'от 400 до 1000 ₽'
  },
  {
    name: 'Колба',
    price: 'от 1000 до 20000 ₽'
  },
  {
    name: 'Шахта',
    price: 'от 5000 ₽'
  },

];
</script>

<style scoped>
.rules__section {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.rules__section--casual {
  max-width: 870px;
  margin: 0 auto;
}

.rules__title, .rules__subtitle {
  color: #9e6850;
  font-weight: 100;
  font-size: 44px;
  line-height: 48px;
  letter-spacing: .1em;
  text-transform: uppercase;
  margin: 80px 0 20px;
  text-align: center;
}
.rules__text {
  margin-top: 8px;
  text-align: center;
}

.rules__block {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.rules__block-article {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.rules__item {
  width: 100%;
  display: grid;
  grid-template-columns: max-content 1fr max-content;
  align-items: start;
}

.rules__item-title {
  font-size: 16px;
  line-height: 120%;
  letter-spacing: .25em;
  text-transform: uppercase;
}

.rules__item-dots {
  border-bottom: 1px dashed #d9d1c9;
  margin: 0 10px;
  height: 16px;
  line-height: 150%;
}

.rules__item-price {
  text-align: end;
}

.rules__section--corkage {
  margin-top: 20px;
}

@media (max-width:768px) {
  .rules__subtitle, .rules__title {
    font-size: 30px;
    margin: 50px 0 20px
  }

  .rules__item-title {
    font-size: 12px;
  }

  .rules__item-dots {
    height: 12px;
  }
}
</style>
