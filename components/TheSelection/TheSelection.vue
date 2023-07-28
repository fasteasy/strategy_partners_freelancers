<template>
  <section class="selection">
    <v-container>
      <h2 class="selection__title text--subtitle">
        Как мы отбираем лучших
      </h2>
      <the-selection-list />
    </v-container>
  </section>
</template>

<style lang="scss" scoped>
.selection__title {
 @include at-desktop {
  margin: 80px 0;
 }
}
</style>
