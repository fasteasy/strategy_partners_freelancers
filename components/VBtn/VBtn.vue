<template>
  <component
    :is="`v-btn-${view}`"
    v-bind="$attrs"
    v-on="$listeners"
  >
    <slot></slot>
  </component>
</template>

<script>
export const VIEW_FILL = 'fill'
export const VIEW_OUTLINE = 'outline'
const views = { VIEW_FILL, VIEW_OUTLINE }

export default {
  props: {
    view: {
      type: String,
      validator: (prop) => Object.values(views).includes(prop),
      default: VIEW_FILL
    }
  },
}
</script>
