<template>
  <ul class="features-list">
    <li
      v-for="item, idx in items"
      :key="idx"
      class="features-list__item"
    >
      <img :src="item.image" class="features-list__item-image">
      <div class="features-list__item-text text--content" v-html="item.text" />
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    items: {
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
.features-list {
  @include at-desktop {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 88px 24px;
  }
}

.features-list__item {
  display: flex;
  @include at-desktop {
    text-align: center;
    flex-direction: column;
    align-items: center;
  }
  @include at-mobile {
    grid-gap: 12px;
    margin-bottom: 40px;
    &:last-child {
      margin-bottom: 0;
    }
  }
}

.features-list__item-image {
  @include at-desktop {
    display: block;
    width: 76px;
    height: 76px;
    margin-bottom: 16px;
  }
  @include at-mobile {
    width: 48px;
    height: 48px;
  }
}

.features-list__item-text {

}
</style>
