<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppMain from './components/AppMain.vue';
export default {
  components: { AppHeader, AppJumbo, AppMain },
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
</template>

<style lang="scss">
@use '../src/assets/scss/style.scss';
</style>
