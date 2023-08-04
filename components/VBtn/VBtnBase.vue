<template>
  <component
    :is="component"
    v-bind="$attrs"
    :disabled="disabled"
    @click.native="($event) => $emit('click', $event)"
    :class="classList"
  >
    <slot />
  </component>
</template>

<script>
const SIZE_MD = 'md'
const SIZE_LG = 'lg'
const sizes = { SIZE_LG, SIZE_MD }

export default {
  props: {
    disabled: {
      type: Boolean,
      default: false
    },
    tag: {
      type: String,
      default: 'button'
    },
    to: {
      type: [String, Object]
    },
    href: {
      type: String
    },
    block: {
      type: Boolean,
      default: false,
    },
    size: {
      type: String,
      validator: (prop) => Object.values(sizes).includes(prop),
      default: SIZE_MD,
    },
  },
  computed: {
    component () {
      if (this.href) return 'a'
      if (this.to) return 'nuxt-link'
      return this.tag
    },
    classList () {
      return [
        'button',
        this.block ? 'button--block' : '',
        this.disabled ? 'button--disabled' : '',
        `button--size-${this.size}`,
      ].filter((item) => item).join(' ')
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
