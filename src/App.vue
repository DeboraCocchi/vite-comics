<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppCta from './components/AppCta.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components:{
    AppHeader,
    AppCta,
    AppFooter,
    AppMain
  }
}

</script>

<template>
  <AppHeader />
  <AppMain />
  <AppCta />
  <AppFooter />
</template>



<style lang="scss">
  @use './style/general';
</style>