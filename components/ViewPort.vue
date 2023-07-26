<template>
  <div class="viewport" :class="classList">
    <slot />
  </div>
</template>

<script>
export default {
  computed: {
    classList () {
      return ''
    }
  }
}
</script>

<style scoped>
.viewport {

}
</style>
