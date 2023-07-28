<template>
  <img v-bind="props" src="./preface.png">
</template>

<script>
import img from './preface.png'
import img2x from './preface2x.png'

export default {
  computed: {
    props() {
      return {
        ...this.$attrs,
        src: img,
        srcset: this.srcset
      }
    },
    srcset () {
      return [
        img,
        img2x ? `${img2x} 2x` : null
      ].filter((item) => item).join(', ')
    }
  }
}
</script>
