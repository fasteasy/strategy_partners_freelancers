<template>
  <v-section class="selection">
    <template #title>
      <div class="selection__inner-container">
        Как мы отбираем лучших
      </div>
    </template>
    <v-container>
      <div class="selection__inner-container">
        <the-selection-list class="selection__list" />
      </div>
    </v-container>
  </v-section>
</template>

<style lang="scss" scoped>
.selection__inner-container {
  @include at-mobile {
    margin-left: auto;
    margin-right: auto;
    max-width: 375px;
  }
}
</style>
