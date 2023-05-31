<script>
    //importo ed esporto i micro-componenti che nel loro insieme compongono l'header
    import AppNavBarVue from './AppNavBar.vue';
    import AppBigBannerVue from './AppBigBanner.vue';

   export default {
    name: "AppHeader",
    components: {
        AppNavBarVue,
        AppBigBannerVue
    }
  }
</script>

<template>
    <!--header-->
    <!--l'header sarà composto da 2 sezioni principali-->
    <header>

        <!--sezione 1-->
        <!--nav-bar-->
        <AppNavBarVue />

        <!--sezione 2-->
        <!--main banner slider-->
        <AppBigBannerVue />

    </header>
</template>

<style lang="scss">
    header{
        background-color: #ffffff;
        height: 50rem;
        width: 100%;
    }
</style>