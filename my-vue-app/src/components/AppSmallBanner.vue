<script>
   export default {
    name: "SmallBanner",

    data(){
      return {
            promo:[
               {
                  img : "./src/assets/images/promo_box_1_bg.jpg",
                  testo1: "70% Off",
                  testo2 : "Vivamus tempor leo lacus, feugiat ut magna aliquam erat.",
                  button : "VIEW MORE",
               },
               {
                  img : "./src/assets/images/promo_box_2_bg.jpg",
                  testo1: "Free Shipping",
                  testo2 : "Vivamus tempor leo lacus, feugiat ut magna aliquam erat.",
                  button : "VIEW MORE",
               }
            ]
         };
       }
   }
</script>

<template>
   <div class="container-fluid align-items-center justify-content-center confettiBox confettiBg">
      <div class="row h-80 align-items-center justify-content-center">
         <div class="col-4 h-100 collection mx-4 d-flex flex-column justify-content-center align-items-start px-5" v-for="promo in promo" :key="promo" :style="'background-image: url(' + promo.img + '); background-size: cover; background-repeat: no-repeat;'">
            <h1 class="text-white">{{ promo.testo1 }}</h1>
            <span class="text-white">{{ promo.testo2 }}</span>
            <button class="bannerBtn text-light rounded-pill px-4 btn my-3">{{ promo.button }}</button>
         </div>
      </div>
   </div>
</template>

<style lang="scss">
   .confettiBox{
      height: 550px;
      background-color: #f4f8f9;
      padding-top: 90px;
   }
   .h-80{
      height: 80%;
   }
   .confettiBg {
      background-image: url(../assets/images/bkgd_confetti-compressor.jpg);
      background-size: contain;
   }
</style>