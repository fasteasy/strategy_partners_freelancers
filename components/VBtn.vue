<template>
  <component
    class="button"
    :class="classList"
    :is="component"
    v-bind="$attrs"
    @click.native="($event) => $emit('click', $event)"
  >
    <slot></slot>
  </component>

</template>

<script>
export const VIEW_PRIMARY = 'primary'
export const VIEW_OUTLINE = 'outline'

export const SIZE_MD = 'md'

const views = { VIEW_PRIMARY, VIEW_OUTLINE }
const sizes = { SIZE_MD }

export default {
  props: {
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
    size: {
      type: String,
      validator: (prop) => Object.values(sizes).includes(prop),
      default: SIZE_MD,
    },
    view: {
      type: String,
      validator: (prop) => Object.values(views).includes(prop),
      default: VIEW_PRIMARY
    }
  },
  computed: {
    classList () {
      return [
      `button--view-${this.view}`,
      `button--size-${this.size}`,
      ].join(' ')
    },
    component () {
      if (this.href) return 'a'
      if (this.to) return 'nuxt-link'
      return this.tag
    }
  }
}
</script>

<style scoped>
.button {
  -webkit-appearance: none;
  border: none;
  background: none;
  padding: 0;
  margin: 0;
  text-align: center;
  border-radius: 0;
  color: inherit;
  font-size: inherit;
  font-weight: inherit;
  font-style: inherit;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  font-family: var(--font-special);
}

.button--size-md {
  height: 60px;
  font-size: 18px;
  border-radius: 30px;
  min-width: 150px;
  padding: 0 20px;
}

.button--view-primary {
  color: #fff;
  font-weight: 300;
  background: linear-gradient(#0EBDAD, #19A0FA);
}

.button--view-outline {
  border: 1px solid
}
</style>
