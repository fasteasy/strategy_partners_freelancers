<template>
  <div class="hero-background" />
</template>

<style lang="scss" scoped>
.hero-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  @include at-desktop {
    background-position: 40% 50%;
    background-image: url('./header-wide.jpg');
  }
  @include at-mobile {
    background-position: 50% 50%;
    background-image: url('./header.jpg');
  }
}
</style>
