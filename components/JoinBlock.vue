<template>
  <v-section class="news-section" :class="classList">
    <v-container>
      <div class="carera-response__block">
        <div class="carera-response__block-title h2">
          Готовы с нами работать?
          <br>
          Присоединяйтесь!
        </div>
        <div class="center btn-border-green__button" style="max-width: 320px; margin-left: auto; margin-right: auto">
          <VBtnRegistration
            style="width: 100%"
            :view="view === VIEW_GREEN ? 'green' : 'space'"
          />
        </div>
      </div>
    </v-container>
  </v-section>
</template>

<script>
export const VIEW_GREEN = 'green'
export const VIEW_WHITE = 'white'
const views = { VIEW_GREEN, VIEW_WHITE }

export default {
  props: {
    view: {
      type: String,
      validator: (prop) => Object.values(views).includes(prop),
      required: true
    }
  },
  data () {
    return {
      VIEW_GREEN,
      VIEW_WHITE,
    }
  },
  computed: {
    classList () {
      return [
        `news-section--view-${this.view}`
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.news-section--view-green {
  background: $background-primary;
}

.news-section--view--white {
  background: #fff;
}
</style>
