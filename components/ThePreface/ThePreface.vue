<template>
  <div class="preface">
    <v-container class="preface__inner">
      <the-preface-image class="preface__image" loading="lazy" />
      <div class="preface__content">
        <h2 class="text--title preface__title text--gradient">
          Уникальные возможности для талантливых специалистов
        </h2>
        <div class="preface__text">
          <p class="text--content">
            Работа с&nbsp;компанией Strategy Partners открывает большие возможности для профессионального роста.
          </p>
          <p class="text--content">
            Мы&nbsp;позволяем независимым экспертам получить доступ к&nbsp;интересным проектам компании и&nbsp;сотрудничать с&nbsp;профессионалами высокого уровня.
          </p>
          <p class="text--content">
            Проходите регистрацию на&nbsp;нашей платформе и&nbsp;узнавайте первыми об&nbsp;открытых вакансиях в&nbsp;штат и&nbsp;на&nbsp;проекты по&nbsp;вашей специальности.
          </p>
        </div>
        <div class="preface__button">
          <registration-button size="lg" view="outline" block>Регистрация</registration-button>
        </div>
      </div>
    </v-container>
  </div>
</template>

<style lang="scss" scoped>
.preface {
  @include at-desktop {
    padding: 60px 0 100px;
  }
  @include at-mobile {
    padding: 20px 0 40px
  }
}
.preface__inner {
  position: relative;
}
.preface__content {
  @include at-desktop {
    width: 526px;
    margin-left: auto;
  }
}
.preface__title {
  margin-bottom: 1.1em
}
.preface__image {
  display: block;
  max-width: 100%;
  @include at-desktop {
    position: absolute;
    top: -11%;
    left: -8%;
    width: 70%;
  }
}
.preface__text {
  // // line-height: 1.45em;
  // & > * {
  //   margin-bottom: 0.75em;
  // }
}

.preface__button {
  @include at-desktop {
    max-width: 320px;
    margin-top: 46px;
  }
  @include at-mobile {
    margin-top: 40px;
  }
}
</style>
