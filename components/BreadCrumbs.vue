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
$gap: 10px;
.breadcrumbs {
  display: flex;
  align-items: center;
  grid-gap: $gap;
  font-size: 16px;
  & > * {
    display: flex;
    grid-gap: $gap;
    &:before {
      content: '/';
      display: block;
    }
    &:first-child:before {
      display: none;
    }
  }
}
</style>
