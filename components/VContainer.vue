<template>
  <div class="container" :class="classList">
    <slot></slot>
  </div>
</template>

<script>
export default {
  computed: {
    classList () {
      const size = this.$viewport.match('desktop') ? 'desktop' : 'mobile'
      return `container--${size}`
    }
  }
}
</script>

<style scoped>
.container {
  height: 20px;
  background: green;
}

.container--mobile {
  margin-right: var(--side-gap);
  margin-left: var(--side-gap);
}

.container--desktop {
  margin-left: auto;
  margin-right: auto;
  width: 1294px;
}
</style>
