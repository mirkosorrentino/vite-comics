<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppBanner,
    AppFooter
  }
}
</script>

<template>
    <AppHeader/>
    <AppMain/>
    <AppBanner/>
    <AppFooter/>
</template>

<style lang="scss" scoped>
@use "./style/general.scss";


</style>
