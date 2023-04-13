<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppBanner from './components/AppBanner.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppBanner,
    AppFooter,
  }

}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppBanner />
  <AppFooter />
</template>


<style lang="scss">
@use "./style/general.scss" as *;
</style>