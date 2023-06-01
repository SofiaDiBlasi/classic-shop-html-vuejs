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
               },
               {
                  img : "./src/assets/images/spring_collection_bg.jpg",
                  testo1: "Spring Collection",
                  testo2 : "BRIGHT AND COLORFUL",
               },
               {
                  img : "./src/assets/images/autumn_collection_bg.jpg",
                  testo1: "Autumn Collection",
                  testo2 : "RICH AND COMFORTABLE",
               }
            ]
         };
      }
   }
</script>

<template>
   <div class="container-fluid mt-3 collectionBox">
      <div class="row h-100">
         <div class="col h-100" v-for="collection in season" :key="collection" :style="'background-image: url(' + collection.img + '); background-size: cover; background-repeat: no-repeat;'">
            <div class="row row-cols-1 h-100">
               <div class="col h-50"></div>
                  <div class="h-50 col d-flex flex-column align-items-center justify-content-center">
                     <h1 class="text-white">{{ collection.testo1 }}</h1>
                     <span class="text-white">{{ collection.testo2 }}</span>
                     <button class="bannerBtn text-light rounded-pill btn btn-lg mt-4 px-4">VIEW MORE</button>
                </div>
            </div>
         </div>
      </div>
   </div>
</template>

<style lang="scss">
   .collectionBox{
      height: 550px;
   }
</style>