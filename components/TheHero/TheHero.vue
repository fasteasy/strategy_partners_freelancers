<template>
  <section class="hero">
    <v-container>
      <bread-crumbs class="hero__nav">
        Root / Here
      </bread-crumbs>
      <div class="hero__heading">
        <h1 class="text--title hero__title">
          Мы приглашаем вас принять участие в&nbsp;уникальных проектах Strategy Partners
        </h1>
        <div class="hero__button">
          <v-btn block>Регистрация</v-btn>
        </div>
      </div>
    </v-container>
  </section>
</template>

<style scoped lang="scss">
.hero {
  background: #eee;
  @include at-desktop {
    padding: 42px 0 104px
  }
}
.hero__heading {
  max-width: 634px;
  @media (--mobile) {
    color: orange
  }
}

.hero__button {
  @include at-desktop {
    margin-top: 50px;
    max-width: 320px;
  }
}
</style>
