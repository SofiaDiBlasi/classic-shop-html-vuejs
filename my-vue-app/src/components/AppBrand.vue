<script>
   export default {
    name: "Brand",
      data() {
         return {
            img:[
               "./src/assets/images/b_logotype_6.png",
               "./src/assets/images/b_logotype_7.png",
               "./src/assets/images/b_logotype_1.png",
               "./src/assets/images/b_logotype_2.png",
               "./src/assets/images/b_logotype_3.png"
            ]
         }
      }
   }
</script>

<template>
   <!--contenitore generale-->
   <div class="container-fluid brandBox py-5">

      <!--testo-->
      <div class="row text-center">
         <p class="">BRAND LOGOS</p>
      </div>

      <!--brand-->
      <div class="row">
         <div class="col d-flex justify-content-center align-items-center">
            <img class="m-5" v-for="img in img" :key="img" :src="img" alt="">
         </div>
      </div>
   </div>
</template>

<style lang="scss">
   .brandBox{
      height: 18.75rem ;
      background-color: #f6f6f6;
   }
</style>