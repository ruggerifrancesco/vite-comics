<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';

  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter
    }
  }
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
  @import './styles/general.scss';
  @import './styles/partials/_mixins';
  @import './styles/partials/_variables';
</style>
