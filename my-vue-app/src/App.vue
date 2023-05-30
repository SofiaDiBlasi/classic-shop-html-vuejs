<script>
  //importo ed esporto i componenti che comporranno il mio layout
  import AppHeaderVue from './components/AppHeader.vue';
  import AppMainVue from './components/AppMain.vue';
  import AppFooterVue from './components/AppFooter.vue';

  export default {
    components: {
      AppHeaderVue,
      AppMainVue,
      AppFooterVue
    }
  }
</script>

<template>
  <div>
    <!--HEADER-->
    <AppHeaderVue />

    <!--MAIN-->
    <AppMainVue />
    
    <!--FOOTER-->
    <AppFooterVue />
  </div>
</template>

<style>
</style>
