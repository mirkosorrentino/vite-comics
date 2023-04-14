<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbotron from './components/AppJumbotron.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppBanner,
    AppFooter,
    AppJumbotron
  }
}
</script>

<template>
    <AppHeader/>
    <AppJumbotron/>
    <AppMain/>
    <AppBanner/>
    <AppFooter/>
</template>

<style lang="scss">
@use "./style/general.scss";

</style>
