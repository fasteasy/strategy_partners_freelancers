<template>
  <section class="hero">
    <the-hero-background class="hero__background" />
    <v-container class="hero__inner">
      <bread-crumbs class="hero__nav" />
      <div class="hero__heading">
        <h1 class="text--title hero__title">
          Мы приглашаем вас принять участие в&nbsp;уникальных проектах Strategy Partners
        </h1>
        <div class="hero__button">
          <VBtnRegistration block view="green" />
        </div>
      </div>
    </v-container>
  </section>
</template>

<style scoped lang="scss">
.hero {
  position: relative;
  @include at-desktop {
    padding: 42px 0 104px
  }
  @include at-mobile {
    padding: 28px 0 40px
  }
}

.hero__inner {
  position: relative;
  z-index: 2;
}

.hero__nav {
  @include at-desktop {
    margin-bottom: 100px;
  }
  @include at-mobile {
    margin-bottom: 80px;
  }
}

.hero__heading {
  max-width: 684px;
  @include at-mobile {
    max-width: 375px;
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
  @include at-mobile {
    margin-top: 32px;
  }
}
</style>
