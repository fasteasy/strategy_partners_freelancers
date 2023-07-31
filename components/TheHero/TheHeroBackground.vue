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
  background: url('./back.png'), $background-primary;
  background-size: auto 100%;
  background-position: 150% 50%;
  background-repeat: no-repeat;
  @include at-mobile {
    background-position: -35% 100%;
    opacity: 0.55;
  }
}

.hero-background:after {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to top, #fff 5%, rgba(255, 255, 255, 0) 50%);
}

.hero-background:before {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(45deg, rgba(255, 255, 25, 0) 40%, #7CFAA4)
}
</style>
