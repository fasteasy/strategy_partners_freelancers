<template>
  <v-section title="Почему нас выбирают" class="features">
    <v-container>
      <v-container>
        <the-features-list :items="items" />
      </v-container>
    </v-container>
  </v-section>
</template>

<script>
import think from './icons/career-think.svg'
import corporate from './icons/career-corporate.svg'
import ecosystem from './icons/career-ecosystem.svg'
import menthors from './icons/career-menthors.svg'
import chat from './icons/career-chat.svg'
import gift from './icons/career-gift.svg'
import party from './icons/career-party.svg'
import stable from './icons/career-stable.svg'
import target from './icons/career-target.svg'

export default {
  computed: {
    items () {
      return [
        {
          image: think,
          text: `Уникальные и&nbsp;значимые<br/> проекты`
        },
        {
          image: corporate,
          text: 'Знакомство с&nbsp;бизнесом крупнейших компаний'
        },
        {
          image: ecosystem,
          text: 'Доступ к&nbsp;образовательным возможностям, передовым технологиям и&nbsp;обмену опытом в&nbsp;экосистеме Сбера'
        },
        {
          image: menthors,
          text: 'Развитая система менторинга и&nbsp;коллективной поддержки'
        },
        {
          image: target,
          text: 'Прозрачные условия <br/> карьерного роста'
        },
        {
          image: stable,
          text: 'Конкурентоспособная оплата и&nbsp;надежность трудоустройства'
        },
        {
          image: gift,
          text: 'Доступ к&nbsp;программам лояльности и&nbsp;бонусам группы Сбера'
        },
        {
          image: party,
          text: 'Насыщенная <br> корпоративная жизнь'
        },
        {
          image: chat,
          text: 'Комфортная культура открытого общения и&nbsp;дружеская среда'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
