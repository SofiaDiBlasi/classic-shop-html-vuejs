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
   <div class="container-fluid brandBox">
      <div class="row">
         <h1>BRAND LOGOS</h1>
      </div>
      <div class="row">
         <div class="col">
            <img v-for="img in img" :key="img" :src="img" alt="">
         </div>
      </div>
   </div>
</template>

<style lang="scss">
   .brandBox{
      background-color: #f6f6f6;
   }
</style>