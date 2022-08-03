<template>
  <app-header />
  <home-page />
  <app-footer />
</template>

<script>
import appHeader from './cmps/app-header.vue'
import homePage from './views/home-page.vue'
import appFooter from './cmps/app-footer.vue'

export default {
  components: {
    appHeader,
    homePage,
    appFooter,
  }
}
</script>