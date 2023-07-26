<template>
  <div class="container">
    <slot></slot>
  </div>
</template>

<style scoped>
.container {
  width: var(--container-width);
  margin-left: var(--container-side);
  margin-right: var(--container-side);
}
</style>
