<script>
   export default {
    name: "AppCollection",

    data(){
      return {
            season:[
               {
               img : "./src/assets/images/winter_collection_bg.jpg",
               testo1: "Winter Collection",
               testo2 : "STYLISH AND WARM",
               button : "VIEW MORE",
               },
               {
                  img : "./src/assets/images/spring_collection_bg.jpg",
                  testo1: "Spring Collection",
                  testo2 : "BRIGHT AND COLORFUL",
                  button : "VIEW MORE",
               },
               {
                  img : "./src/assets/images/autumn_collection_bg.jpg",
                  testo1: "Autumn Collection",
                  testo2 : "RICH AND COMFORTABLE",
                  button : "VIEW MORE",
               }
            ]
      };
    },
   }
</script>

<template>
   <div class="container-fluid collectionBox">
      <div class="row">
         <div class="col-4 collection" v-for="collection in season" :key="collection" :style="'background-image: url(' + collection.img + ')'">
            <h1 class="text-white">{{ collection.testo1 }}</h1>
            <span class="text-white">{{ collection.testo2 }}</span>
            <button class="bannerBtn text-light rounded-pill">{{ collection.button }}</button>
         </div>
      </div>
   </div>
</template>

<style lang="scss">
   .collectionBox{
      background-color: red;
      height: 615px;
   }
   .collection{
      height: 615px;
      background-size: contain;
      background-repeat: no-repeat;
   }
</style>