<template>
  <v-btn-base
    v-bind="$attrs"
    v-on="$listeners"
    class="button--outline"
  >
    <span class="button-outline-text">
      <slot></slot>
    </span>
  </v-btn-base>
</template>

<style lang="scss" scoped>
.button--outline {
  background: #fff;
  border: 1px solid;
  color: $color-blue;
  transition: 0.25s background;
}


.button--outline:hover {
  border-color: transparent;
  color: #fff;
  background: $background-secondary;
}


// .button--outline {
//   background: #fff !important;
//   border: 1px solid;
//   color: $color-blue;
// }

// .button--outline:hover {
//   background: $background-secondary;
//   color: #fff;
//   border-color: $color-blue
// }

// .button--outline:not(:hover) {
//   @include text-gradient;
// }

// .button-outline-text {

// }
</style>
