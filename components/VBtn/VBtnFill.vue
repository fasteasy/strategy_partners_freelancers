<template>
  <v-btn-base
    v-bind="$attrs"
    v-on="$listeners"
    class="button--fill"
  >
    <slot></slot>
  </v-btn-base>
</template>

<style lang="scss" scoped>
.button--fill {
  color: #fff;
  background: $background-secondary;
  &:hover {
    background: $color-blue;
  }
  &:active {
    background: $color-blue;
  }
}

</style>
