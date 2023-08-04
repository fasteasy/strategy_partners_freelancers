<template>
  <section class="section section_white">
    <div class="section__title" v-if="title || $scopedSlots.title">
      <v-container>
        <component :is="titleTag" class="text--title">
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
  @include at-mobile {
    padding-top: 40px;
    padding-bottom: 40px;
  }
}

.section__title {
  @include at-mobile {
    margin-bottom: 60px;
  }
  @include at-desktop {
    margin-bottom: 80px;
  }
}
</style>
