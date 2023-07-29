<template>
  <section class="section">
    <div class="section__title" v-if="title || $scopedSlots.title">
      <v-container>
        <component :is="titleTag" class="section__title text--subtitle">
          <slot name="title">
            <span v-html="title" />
          </slot>
        </component>
      </v-container>
    </div>
    <slot></slot>
  </section>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    },
    titleTag: {
      type: String,
      default: 'h2'
    }
  }
}
</script>

<style lang="scss" scoped>
.section {
  @include at-desktop {
    padding-top: 80px;
    padding-bottom: 80px;
  }
}

.section__title {
  @include at-desktop {
    margin-bottom: 80px;
  }
}
</style>
