<script>
  //importo ed esporto i micro-componenti che nel loro insieme compongono il footer
  import AppBrand from './AppBrand.vue';
  import AppSubscribeVue from './AppSubscribe.vue';
  import AppTermsVue from './AppTerms.vue';
  import AppContattiVue from './AppContatti.vue';

  export default {
  name: "AppFooter",
  components: {
    AppBrand,
    AppSubscribeVue,
    AppTermsVue,
    AppContattiVue
  }
}
</script>

<template>
  <!--footer-->
  <!--ho identificato nel footer 4 sezioni-->
  <footer>

    <!--sezione 1-->
    <!--Brand all'interno dell'ecommerce-->
    <AppBrand />

    <!--sezione 2-->
    <!--Sezione in cui fare subscribe-->
    <AppSubscribeVue />

    <!--sezione 3-->
    <!--Info azienda etc-->
    <AppContattiVue />
    

    <!--sezione 4-->
    <!--Copyright etc-->
    <AppTermsVue />
   

  </footer>
</template>

<style>
    footer{
        width: 100%;
        height: 71.875rem;
    }
</style>