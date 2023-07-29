<template>
  <div class="container">
    <slot></slot>
  </div>
</template>

<style scoped lang="scss">
.container {
  max-width: 131rem;
  margin-left: auto;
  margin-right: auto;
  @include at-mobile {
    margin-left: 2rem;
    margin-right: 2rem;
  }
}
</style>
