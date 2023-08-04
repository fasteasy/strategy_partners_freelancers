<template>
  <v-section class="preface">
    <v-container>
      <div class="preface__content">
        <div class="preface__content-aside">
          <the-preface-image class="preface__image" loading="lazy" />
        </div>
        <div class="preface__content-main">
          <h1 class="preface__title text--gradient">
            Уникальные возможности для талантливых специалистов
          </h1>
          <div class="preface__text">
            <p>
              Работа с&nbsp;компанией Strategy Partners открывает большие возможности для профессионального роста.
            </p>
            <p>
              Мы&nbsp;позволяем независимым экспертам получить доступ к&nbsp;интересным проектам компании и&nbsp;сотрудничать с&nbsp;профессионалами высокого уровня.
            </p>
            <p>
              Проходите регистрацию на&nbsp;нашей платформе и&nbsp;узнавайте первыми об&nbsp;открытых вакансиях в&nbsp;штат и&nbsp;на&nbsp;проекты по&nbsp;вашей специальности.
            </p>
          </div>
          <div class="preface__button">
            <VBtnRegistration block view="space" />
          </div>
        </div>
      </div>
    </v-container>
  </v-section>
</template>

<style lang="scss" scoped>
.preface {
  @include at-desktop {
    padding: 60px 0 100px;
  }
  @include at-mobile {
    overflow: hidden;
    padding: 20px 0 40px;
  }
}

.preface__content {
  @media screen and (min-width: 640px) {
    display: grid;
    grid-template-columns: auto 52%;
  }
  @include at-desktop {
    grid-template-columns: auto 46%;
  }
}

.preface__content-aside {
  position: relative;
}

.preface__content-main {
  @media screen and (max-width: 639px) {
    margin-top: -30px;
  }
}

.preface__title p {
  @include at-desktop {
    font-size: 40px;
  }
  @include at-mobile {
    font-size: 22px;
  }
}
.preface__image {
  @include at-desktop {
    position: absolute;
    top: -4%;
    left: -4%;
    max-width: 110%;
  }
  @include at-mobile {
    position: relative;
    // left: 50%;
    // width: 123%;
    max-width: 475px;
    width: 100%;
    // transform: translateX(-50%)
  }
}
.preface__text p {
  margin-bottom: 1em;
  @include at-desktop {
    font-size: 24px;
  }
  @include at-mobile {
    font-size: 18px;
  }
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
