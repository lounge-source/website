<script setup>
const hookahs = [
  {
    name: 'Standard',
    price: '1000 ₽'
  },
 {
    name: 'Premium Hard',
    price: '1200 ₽'
  },
 {
    name: 'Второй кальян',
    price: '900 ₽'
  },
  {
    name: 'Дневной кальян',
    price: '750 ₽'
  },
]

const hookahsRules = [
  {
    name: 'До 4 человек',
    price: '1 кальян'
  },
  {
    name: 'Более 4 человек',
    price: '2 кальяна'
  },
  {
    name: 'Более 7 человек',
    price: '3 кальяна'
  },
]
</script>

<template>
  <div class="hookah-menu">
    <h2 class="hookah-menu__title">Кальян</h2>

    <div class="hookah__block">
      <div v-for="(hookah) in hookahs" class="hookah__block-article">
        <div class="hookah__item">
          <p class="hookah__item-title">{{ hookah.name }}</p>
          <div class="hookah__item-dots"></div>
          <p class="hookah__item-price">{{ hookah.price }}</p>
        </div>
      </div>
    </div>

    <h3 class="hookah-menu__title">Правила подачи кальяна</h3>

    <div class="hookah__block">
      <div v-for="(rule) in hookahsRules" class="hookah__block-article">
        <div class="hookah__item">
          <p class="hookah__item-title">{{ rule.name }}</p>
          <div class="hookah__item-dots"></div>
          <p class="hookah__item-price">{{ rule.price }}</p>
        </div>
      </div>
    </div>
    <div class="hookah-menu__miscellaneous-container">
      <div class="hookah-menu__item">
        <p class="hookah-menu__item-detail">90 минут</p>
        <p class="hookah-menu__item-info">Максимальное время курения с момента подачи</p>
      </div>
      <div class="hookah-menu__item">
        <p class="hookah-menu__item-detail">10% скидка</p>
        <p class="hookah-menu__item-info">В день рождения на весь чек (кальяны, бар)</p>
      </div>
    </div>

  </div>

</template>

<style scoped>
.hookah-menu {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.hookah-menu__title {
  color: #9e6850;
  font-weight: 100;
  font-size: 44px;
  line-height: 48px;
  letter-spacing: .1em;
  text-transform: uppercase;
  margin: 80px 0 20px;
  text-align: center;
}

.hookah__block {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.hookah__block-article {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.hookah-menu__miscellaneous-container {
  display: flex;
  flex-wrap: wrap;
  margin-top: 10px;
  text-align: center;
  text-transform: uppercase;
  font-size: 14px;
}

.hookah-menu__miscellaneous-container > * {
  width: 100%;
}

.hookah-menu__miscellaneous-container > .hookah-menu__item {
  padding: 10px;
}

.hookah-menu__miscellaneous-container .hookah-menu__item-detail {
  color: #9e6850;
  font-weight: 300;
  font-size: 22px;
  line-height: 48px;
  letter-spacing: .1em;
  text-transform: uppercase;
  text-align: center;
}

@media (min-width:768px) {
  .hookah-menu__miscellaneous-container > * {
    width: 50%;
  }
}

.hookah__item {
  width: 100%;
  display: grid;
  grid-template-columns: max-content 1fr max-content;
  align-items: start;
}

.hookah__item-title {
  font-size: 16px;
  line-height: 120%;
  letter-spacing: .25em;
  text-transform: uppercase;
}

.hookah__item-dots {
  border-bottom: 1px dashed #d9d1c9;
  margin: 0 10px;
  height: 16px;
  line-height: 150%;
}

.hookah__item-price {
  text-align: end;
}

@media (max-width:768px) {
  .hookah-menu__title {
    font-size: 30px;
    margin: 50px 0 20px;
  }

  .hookah__item-title {
    font-size: 12px;
  }

  .hookah__item-dots {
    height: 12px;
  }

  .hookah-menu__item-detail {
    font-size: 20px;
  }

  .hookah-menu__item-info {
    font-size: 12px;
  }

  .hookah-menu__miscellaneous-container {
    .hookah-menu__item {
      padding: 6px;
    }
  }


}
</style>
