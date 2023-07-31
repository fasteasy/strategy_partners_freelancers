<template>
  <v-section title="Как мы отбираем лучших" class="selection">
    <v-container>
      <the-selection-list class="selection__list" />
    </v-container>
  </v-section>
</template>

<style lang="scss" scoped>
.selection__list {
  @include at-mobile {
    margin-top: 60px;
  }
}
</style>
