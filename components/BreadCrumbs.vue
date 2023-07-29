<template>
  <ul class="breadcrumbs">
    <li
      v-for="item in items" :key="item.label"
      class="breadcrumbs__item"
      :class="item.url ? 'active' : null"
    >
      <component
        :is="item.url ? 'a' : 'span'"
        :href="item.url ? item.url : undefined"
        :class="item.url ? 'breadcrumbs__item-link' : 'breadcrumbs__item-text'"
      >
        {{ item.label }}
      </component>
    </li>
  </ul>
</template>

<script>
export default {
  computed: {
    items () {
      return [
        {
          label: 'Главная',
          url: '/',
        },
        {
          label: 'Карьера',
          url: '/career',
        },
        {
          label: 'Фрилансерам',
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
$gap: 12px;
.breadcrumbs {
  display: flex;
  align-items: center;
  grid-gap: $gap;
  @include at-desktop {
    font-size: 1.6em;
    line-height: 2.4rem;
  }
}

.breadcrumbs__item {
  display: flex;
  grid-gap: $gap;
  &:before {
    color: #505354;
    opacity: 0.7;
    content: '/';
    display: block;
    font-size: 20px;
  }
  &:first-child:before {
    display: none;
  }
  &.active {
    opacity: 1;
  }
}

.breadcrumbs__item-link {
  color: $color-blue;
  &:hover {
    text-decoration: underline;
  }
}

.breadcrumbs__item-text {
  color: #505354;
  opacity: 0.7;
}
</style>
