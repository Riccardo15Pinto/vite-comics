<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
export default {
  components: { AppHeader, AppJumbo },
  data() {
    return {

    }
  }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
</template>

<style lang="scss">
@use '../src/assets/scss/style.scss';
</style>
