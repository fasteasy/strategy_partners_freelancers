<template>
  <section class="hero">
    <the-hero-background class="hero__background" />
    <v-container class="hero__inner">
      <bread-crumbs class="hero__nav">
        Root / Here
      </bread-crumbs>
      <div class="hero__heading">
        <h1 class="text--title hero__title">
          Мы приглашаем вас принять участие в&nbsp;уникальных проектах Strategy Partners
        </h1>
        <div class="hero__button">
          <registration-button block>Регистрация</registration-button>
        </div>
      </div>
    </v-container>
  </section>
</template>

<style scoped lang="scss">
.hero {
  position: relative;
  background: #eee;
  @include at-desktop {
    padding: 42px 0 104px
  }
}

.hero__inner {
  position: relative;
}

.hero__nav {
  margin-bottom: 100px;
}

.hero__heading {
  max-width: 684px;
  @media (--mobile) {
    color: orange
  }
}

.hero__title {
  text-shadow: 1px 1px 14px #fff;
}

.hero__button {
  @include at-desktop {
    margin-top: 40px;
    max-width: 320px;
  }
}
</style>
