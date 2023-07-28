<template>
  <div class="container">
    <slot></slot>
  </div>
</template>

<style scoped lang="scss">
.container {
  margin-left: var(--gap);
  margin-right: var(--gap);

  @include at-desktop-wide {
    width: 1296px;
    margin-left: auto;
    margin-right: auto;

  }
}
</style>
