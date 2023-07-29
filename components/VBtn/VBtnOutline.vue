<template>
  <v-btn-base
    v-bind="$attrs"
    :class="classList"
    v-on="$listeners"
  >
    <span class="button__text text--gradiend">
      <slot></slot>
    </span>
  </v-btn-base>
</template>

<script>
const SIZE_MD = 'md'
const SIZE_LG = 'lg'
const sizes = { SIZE_LG, SIZE_MD }

export default {
  props: {
    size: {
      type: String,
      validator: (prop) => Object.values(sizes).includes(prop),
      default: SIZE_MD,
    },
  },
  computed: {
    classList () {
      return [
        `button--size-${this.size}`,
        `button--outline`
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
$sizes: (
  lg: (
    height: 60px
  ),
  md: (
    height: 40px
  )
);

.button--outline {
  background: #fff;
  border: 1px solid;
  @each $key, $size in $sizes {
    &--#{$key} {
      color: green;
      // height: map-get($size, height)
    }
  }
}
</style>
