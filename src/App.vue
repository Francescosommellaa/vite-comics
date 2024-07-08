<script>
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue';
import AppSeries from './components/AppSeries.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppHero,
    AppSeries,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader/>
  <AppHero/>
  <AppSeries/>
  <AppFooter/>
</template>

<style lang="scss">
  @use './styles/partials/mixins' as *;
  @use './styles/partials/variables' as *;
  @use './styles/general.scss' as *;
</style>
