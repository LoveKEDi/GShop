<template>
  <div id="app">
    <router-view></router-view>
    <footer-guide v-show="$route.meta.showFooter"></footer-guide>
  </div>
</template>

<script>
import FooterGuide from './components/FooterGuide/FooterGuide.vue'
import {mapActions} from 'vuex'
export default {
  name: 'App',
  components: {
    FooterGuide
  },
  mounted () {
    this.getAddress()
  },
  methods: {
    ...mapActions(['getAddress'])
  }
}
</script>

<style lang="stylus">
  #app
    width: 100%
    height: 100%
    background: #f5f5f5
</style>
