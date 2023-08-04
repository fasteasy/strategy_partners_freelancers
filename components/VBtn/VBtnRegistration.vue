<template>
  <component
    :is="component"
    v-bind="{ ...$attrs, href: $d.registrationURL }"
    :class="block ? 'btn--block' : ''"
    v-on="$listeners"
  >
    Регистрация
  </component>
</template>

<script>
export const VIEW_SPACE = 'space'
export const VIEW_GREEN = 'green'
const views = { VIEW_SPACE, VIEW_GREEN }

export default {
  props: {
    block: {
      type: Boolean,
      default: false
    },
    view: {
      type: String,
      validator: (prop) => Object.values(views).includes(prop),
      required: true,
    }
  },
  computed: {
    component () {
      return {
        [VIEW_SPACE]: 'VBtnSpace',
        [VIEW_GREEN]: 'VBtnGreen',
      }[this.view]
    }
  }
}
</script>

<style lang="scss" scoped>
.btn--block {
  width: 100%;
}
</style>
