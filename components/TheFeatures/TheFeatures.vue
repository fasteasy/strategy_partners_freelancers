<template>
  <v-section title="Почему нас выбирают" class="features">
    <v-container>
      <the-features-list :items="items" />
      <join-block class="features__footer" />
    </v-container>
  </v-section>
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
          text: `Уникальные и&nbsp;значимые<br/> проекты`
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
          text: 'Прозрачные условия <br/> карьерного роста'
        },
        {
          image: img6,
          text: 'Конкурентоспособная оплата и&nbsp;надежность трудоустройства'
        },
        {
          image: img7,
          text: 'Доступ к&nbsp;программам лояльности и&nbsp;бонусам группы Сбера'
        },
        {
          image: img8,
          text: 'Насыщенная <br> корпоративная жизнь'
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
}
.features__footer {
  margin-top: 80px;
}

</style>
