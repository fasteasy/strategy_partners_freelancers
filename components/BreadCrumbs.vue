<template>
  <ul class="breadcrumbs">
    <li v-for="item in items" :key="item.label">
      <a :href="item.url">{{ item.label }}</a>
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
          url: '/'
        },
        {
          label: 'Карьера',
          url: '/career'
        },
        {
          label: 'Фрилансерам'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
$gap: 12px;
.breadcrumbs {
  font-family: var(--font-special);
  display: flex;
  align-items: center;
  grid-gap: $gap;
  font-size: 16px;
  line-height: 20px;
  & > * {
    display: flex;
    grid-gap: $gap;
    &:before {
      content: '/';
      display: block;
      font-size: 20px;
    }
    &:first-child:before {
      display: none;
    }
  }
}
</style>
