<template>
  <ul class="selection-list">
    <li
      class="selection-list__item"
      v-for="item, idx in items"
      :key="idx"
    >
      <div class="selection-list__item-number" :style="{ backgroundImage: `url(${item.number})` }" />
      <div class="selection-list__item-inner">
        <img :src="item.image" loading="lazy" class="selection-list__item-image" />
        <h3 class="selection-list__item-title text--subtitle" v-html="item.title" />
        <div class="selection-list__item-text" v-html="item.text" />
      </div>
    </li>
  </ul>
</template>

<script>
const numbers = [
  require('./img/1.svg'),
  require('./img/2.svg'),
  require('./img/3.svg')
]
export default {
  computed: {
    items () {
      return [
        {
          image: require('./img/star.svg'),
          title: 'Регистрируйтесь на&nbsp;платформе',
          text: 'Для более эффективного поиска подходящих кандидатур на&nbsp;вакансии предлагаем вам предоставить информацию о&nbsp;своем профессиональном опыте и&nbsp;навыках. Это поможет нам рассмотреть вашу кандидатуру при появлении позиций'
        },
        {
          image: require('./img/hands.svg'),
          title: 'Получайте наше предложение',
          text: 'Если ваш профессиональный опыт и&nbsp;навыки подходят нам &mdash;&nbsp;предлагаем вам заполнить анкету. Мы&nbsp;всегда готовы рассмотреть вашу кандидатуру и&nbsp;обсудить детали возможного партнерства'
        },
        {
          image: require('./img/chart.svg'),
          title: 'Приступайте к&nbsp;работе в&nbsp;команде SP',
          text: 'Присоединяйтесь к&nbsp;команде профессионалов и&nbsp;начинайте решать уникальные задачи совместно с&nbsp;SP. Делитесь своим опытом с&nbsp;коллегами и&nbsp;добивайтесь новых высот в&nbsp;амбициозной компании. Мы&nbsp;вам всегда рады!'
        }
      ].map((item, idx) => ({
        ...item,
        number: numbers[idx]
      }))
    }
  }
}
</script>

<style lang="scss" scoped>
.selection-list {
  @include at-desktop {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 24px;
  }
}

.selection-list__item {
  position: relative;
}

.selection-list__item-number {
  @include at-desktop {
    position: absolute;
    top: 250px;
    left: -20%;
    width: 100%;
    height: 100%;
    background-size: auto;
    background-position: 0 0;
    background-repeat: no-repeat;
  }
}

.selection-list__item-inner {
  position: relative;
}

.selection-list__item-image {
  @include at-desktop {
    margin-bottom: 40px;
  }
}

.selection-list__item-title {
  @include at-desktop {
    margin-bottom: 20px;
  }
}

.selection-list__item-text {
  @include at-desktop {
    line-height: 36px;
    padding-right: 90px;
  }
}
</style>
