<template>
  <div class="join">
    <v-container>
      <join-block />
    </v-container>
  </div>
</template>

<style lang="scss" scoped>
.join {
  background: $background-primary;
  @include at-desktop {
    padding: 94px 0 74px;
  }
  @include at-mobile {
    padding-top: 40px;
    padding-bottom: 40px;
  }
}
</style>
