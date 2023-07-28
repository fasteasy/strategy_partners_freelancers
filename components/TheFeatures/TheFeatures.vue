<template>
  <section class="features">
    <v-container>
      <h2 class="features__title text--subtitle">
        Почему нас выбирают
      </h2>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus tempora delectus dolor atque, eaque laboriosam illum excepturi inventore, quam iure fugiat natus asperiores doloremque beatae sapiente accusantium officia! Laboriosam, suscipit!
    </v-container>
  </section>
</template>

<style lang="scss" scoped>
.features {
  @include at-desktop {
    padding: 80px 0;
  }
}

.features__title {
  @include at-desktop {
    margin-bottom: 80px;
  }
}
</style>
