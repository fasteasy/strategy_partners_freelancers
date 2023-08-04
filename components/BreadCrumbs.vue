<template>
  <nav aria-label="breacrumbs-main">
    <ol
      class="breadcrumb"
    >
      <li
        class="breadcrumb-item"
        :class="item.url ? 'active' : null"
        v-for="item in items"
        :key="item.label"
        :aria-current="item.label"
      >
        <a :href="item.url" class="breadcrumb-link" v-if="item.url">
          {{ item.label }}
        </a>
        <template v-else>
          {{ item.label }}
        </template>
      </li>
    </ol>
  </nav>
</template>

<script>
export default {
  computed: {
    items () {
      return [
        {
          label: 'Главная',
          url: 'https://strategy.ru/',
        },
        {
          label: 'Карьера',
          url: 'https://strategy.ru/career',
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
</style>
