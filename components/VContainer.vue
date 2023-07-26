<template>
  <div class="container">
    <slot></slot>
  </div>
</template>

<style scoped lang="scss">
.container {
  @include at-mobile {
    margin-left: var(--gap);
    margin-right: var(--gap);
  }
  @include at-desktop {
    width: 1296px;
    margin-left: auto;
    margin-right: auto;

  }
}
</style>
