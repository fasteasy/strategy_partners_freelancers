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
</style>
