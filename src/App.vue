<script>
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue';
import AppSeries from './components/AppSeries.vue';
import AppFooter from './components/AppFooter.vue';

export default {
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

<style scoped></style>
