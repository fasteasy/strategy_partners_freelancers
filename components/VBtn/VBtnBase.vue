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
$sizes: (
  lg: (
    height: 60px
  ),
  md: (
    height: 40px
  )
);
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
  padding: 0 20px;
  min-width: 150px;
  font-size: 18px;
  line-height: 1em;
}
.button--block {
  width: 100%;
  display: flex;
}
.button--disabled {
  pointer-events: none;
  opacity: 0.5;
}

@each $key, $size in $sizes {
  .button--size-#{$key} {
    $height: map-get($size, height);
    height: $height;
    border-radius: $height/2;
  }
}

</style>
