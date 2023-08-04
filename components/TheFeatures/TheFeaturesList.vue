<template>
  <ul class="choise-block__wrap">
    <li
      v-for="item, idx in items"
      :key="idx"
      class="choise-block__column"
    >
      <div class="choise-block__item">
        <div class="choise-block__icon">
          <img :src="item.image" class="choise-block__image">
        </div>
        <div class="choise-block__content" v-html="item.text" />
      </div>
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
</style>
