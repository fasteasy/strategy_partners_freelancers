<template>
  <section class="features">
    <v-container>
      <h2 class="features__title text--subtitle">
        Почему нас выбирают
      </h2>
      <the-features-list :items="items" />

      <div class="features__footer">
        <h3 class="features__footer-title">
          Присоединяйтесь к&nbsp;программе Strategy Experts!
        </h3>
        <div class="features__footer-button">
          <v-btn view="outline" block>Регистрация</v-btn>
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
import img1 from './icons/1.svg'
import img2 from './icons/2.svg'
import img3 from './icons/3.svg'
import img4 from './icons/4.svg'
import img5 from './icons/5.svg'
import img6 from './icons/6.svg'
import img7 from './icons/7.svg'
import img8 from './icons/8.svg'
import img9 from './icons/9.svg'

export default {
  computed: {
    items () {
      return [
        {
          image: img1,
          text: `Уникальные и&nbsp;значимые проекты`
        },
        {
          image: img2,
          text: 'Знакомство с&nbsp;бизнесом крупнейших компаний'
        },
        {
          image: img3,
          text: 'Доступ к&nbsp;образовательным возможностям, передовым технологиям и&nbsp;обмену опытом в&nbsp;экосистеме Сбера'
        },
        {
          image: img4,
          text: 'Развитая система менторинга и&nbsp;коллективной поддержки'
        },
        {
          image: img5,
          text: 'Прозрачные условия карьерного роста'
        },
        {
          image: img6,
          text: 'Конкурентоспособная оплата и&nbsp;надежность трудоустройства'
        },
        {
          image: img7,
          text: 'Доступ к&nbsp;программам лояльности и&nbsp;бонусам группы Сбера'
        },
        {
          image: img8,
          text: 'Насыщенная корпоративная жизнь'
        },
        {
          image: img9,
          text: 'Комфортная культура открытого общения и&nbsp;дружеская среда'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.features {
  @include at-desktop {
    padding: 80px 0;
  }
}
.features__title {
  @include at-desktop {
    margin-bottom: 80px;
  }
}
.features__footer {
  margin: 80px;
  text-align: center
}
.features__footer-title {
  max-width: 500px;
  margin-left: auto;
  margin-right: auto;
}
.features__footer-button {
  margin-top: 30px;
  max-width: 320px;
  margin-left: auto;
  margin-right: auto;
}
</style>
