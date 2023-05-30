<script>
  //importo ed esporto i micro-componenti che nel loro insieme compongono il main
  import AppFeaturedProductsVue from './AppFeaturedProducts.vue';
  import AppCollectionVue from './AppCollection.vue';
  import AppBestSellerVue from './AppBestSeller.vue';
  import AppSmallBannerVue from './AppSmallBanner.vue';
  import AppNewarrivalsVue from './AppNewarrivals.vue';
  import AppTestimonialVue from './AppTestimonial.vue';
  import AppBlogVue from './AppBlog.vue';
  import AppSummaryVue from './AppSummary.vue';

   export default {
    name: "AppMain",
    components: {
      AppFeaturedProductsVue,
      AppCollectionVue,
      AppBestSellerVue,
      AppSmallBannerVue,
      AppNewarrivalsVue,
      AppTestimonialVue,
      AppBlogVue,
      AppSummaryVue
    }
  }
</script>

<template>
  <!--main-->
  <!--ho identificato nel main 8 sezioni suddivise per argomenti-->
  <main>

    <!--sezione 1-->
    <!--Prodotti suddivisi per categorie-->
    <AppFeaturedProductsVue />

    <!--sezione 2-->
    <!--Collezioni per stagione-->
    <AppCollectionVue />

    <!--sezione 3-->
    <!--Best-Seller primo slider carosello-->
    <AppBestSellerVue />

    <!--sezione 4-->
    <!--Banner più piccolo con promozioni-->
    <AppSmallBannerVue />

    <!--sezione 5-->
    <!--Nuovi arrivi secondo slider carosello-->
    <AppNewarrivalsVue />

    <!--sezione 6-->
    <!--Testimonial-->
    <AppTestimonialVue />

    <!--sezione 7-->
    <!--Blog-->
    <AppBlogVue />

    <!--sezione 8-->
    <!--Riassunto delle parti che devono essere più in vista-->
    <AppSummaryVue />

  </main>
</template>