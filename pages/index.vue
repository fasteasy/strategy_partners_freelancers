<template>
  <v-container>
    <v-btn type="button">ad</v-btn>
    <v-btn view="outline">ad</v-btn>

    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatem accusamus totam necessitatibus quisquam, laboriosam doloribus aspernatur cupiditate inventore repudiandae repellendus, tenetur ex ratione id dolorum enim rerum corrupti libero illum!
  </v-container>
</template>

<script>
export default {
  mounted () {
    console.log(this.$viewport)
  }
}
</script>
