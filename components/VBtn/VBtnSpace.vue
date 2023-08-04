<template>
  <component
    :is="component"
    v-bind="{ ...$attrs, to, href }"
    v-on="$listeners"
    class="btn-space btn-border-green btn-border-green--large"
  >
    <span class="btn-space__text btn-border-green__text">
      <slot></slot>
    </span>
  </component>
</template>

<script>
export default {
  props: {
    tag: {
      type: String,
      default: 'button'
    },
    href: {
      type: String
    },
    to: {
      type: [Object, String]
    }
  },
  computed: {
    component () {
      if (this.to) return 'nuxt-link'
      if (this.href) return 'a'
      return this.tag
    }
  }
}
</script>

<style lang="scss" scoped>
// .btn-space {
//   height: 60px;
//   border-radius: 30px;
//   &:before {
//     border-radius: 32px;
//   }
// }
</style>
