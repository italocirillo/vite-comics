<script>
import AppHeader from './components/AppHeader.vue';
import AppCardHero from './components/AppCardHero.vue';
import AppFooter from './components/AppFooter.vue';
import AppBanner from './components/AppBanner.vue';

export default {
  components: {
    AppHeader,
    AppCardHero,
    AppBanner,
    AppFooter,
  }

}
</script>

<template>
  <AppHeader />
  <AppCardHero />
  <AppBanner />
  <AppFooter />
</template>


<style lang="scss">
@use "./style/general.scss" as *;
</style>