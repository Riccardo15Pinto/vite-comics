<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.Vue'
export default {
  components: { AppHeader, AppJumbo, AppMain, AppFooter },
  data() {
    return {

    }
  }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use '../src/assets/scss/style.scss';
</style>
