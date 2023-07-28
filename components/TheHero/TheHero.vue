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
        <v-btn>Регистрация</v-btn>
      </div>
    </v-container>
  </section>
</template>

<style scoped lang="scss">
.hero {
  background: #eee;
}
.hero__heading {
  max-width: 634px;
  @media (--mobile) {
    color: orange
  }
}
</style>
