<template>
  <div class="join">
    <v-container>
      <join-button />
    </v-container>
  </div>
</template>

<style lang="scss" scoped>
.join {
  background: $background-primary;
  @include at-desktop {
    padding: 94px 0 74px;
  }
}
</style>
