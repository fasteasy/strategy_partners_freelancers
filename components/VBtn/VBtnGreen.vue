<template>
  <component
    :is="component"
    v-bind="{ ...$attrs, to, href }"
    v-on="$listeners"
    class="btn-green"
  >
    <slot></slot>
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
