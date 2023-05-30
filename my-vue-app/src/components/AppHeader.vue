<script>
    //importo ed esporto i micro-componenti che nel loro insieme compongono l'header
    import AppCartVue from './AppCart.vue';
    import AppNavBarVue from './AppNavBar.vue';
    import AppBigBannerVue from './AppBigBanner.vue';

   export default {
    name: "AppHeader",
    components: {
        AppCartVue,
        AppNavBarVue,
        AppBigBannerVue
    }
  }
</script>

<template>
    <!--header-->
    <!--l'header sarà composto da 3 sezioni principali-->
    <header>

        <!--sezione 1-->
        <!--cart-bar-->
        <AppCartVue />

        <!--sezione 2-->
        <!--nav-bar-->
        <AppNavBarVue />

        <!--sezione 3-->
        <!--main banner-->
        <AppBigBannerVue />

    </header>
</template>