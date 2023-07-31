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
$gap-small: 8px;
.breadcrumbs {
  display: flex;
  align-items: center;
  @include at-desktop {
    font-size: 1.6em;
    line-height: 2.4rem;
    grid-gap: $gap;
  }
  @include at-mobile {
    grid-gap: $gap-small;
  }
}

.breadcrumbs__item {
  display: flex;
  align-items: center;
  &:before {
    color: #505354;
    opacity: 0.7;
    content: '/';
    display: block;
    font-size: 1.5em;
  }
  &:first-child:before {
    display: none;
  }
  &.active {
    opacity: 1;
  }
  @include at-desktop {
    grid-gap: $gap;
  }
  @include at-mobile {
    grid-gap: $gap-small;
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
