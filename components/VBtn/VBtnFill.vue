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
.button.button--fill {
  color: #fff;
  background: $background-secondary;
  transition: 0.15s background;
  &:hover {
    background: $color-blue;
  }
  &:active {
    background: $color-blue;
  }
}

</style>
