<script>
   export default {
    name: "Summary",

    data(){
      return {
         titles : [
            "FEATURED",
            "ON SALE",
            "TOP RATED",
            "LATEST REVIEWS"
         ],
         products : [
          {
            name: "Black Jacket",
            titlePrice : "$125",
            img : "./src/assets/images/black_leather_jacket-120x156.jpg",
          },
          {
            name: "Black Leather Jacket",
            star: 5,
            sales: "$235",
            price : "$200",
            img : "./src/assets/images/black_elegant_leather_jacket-120x156.jpg"
          },
          {
            name: "Leather Gloves",
            star: 5,
            price : "$45",
            img : "./src/assets/images/leather_gloves-120x156.jpg"
          },
          {
            name: "Black Leather Jacket",
            star: 5,
            author: "by admin",
            img : "./src/assets/images/black_elegant_leather_jacket-120x156.jpg"
          },
          {
            name: "Black Leather Jacket",
            star: 5,
            sales: "$235",
            price : "$200",
            img : "./src/assets/images/black_elegant_leather_jacket-120x156.jpg"
          },
          {
            name: "Blue Leather Jacket",
            titlePrice: "$80",
            price : "$60",
            img : "./src/assets/images/blue_leather_jacket-120x156.jpg"
          },
          {
            name: "Black Leather Jacket",
            star: 5,
            sales: "$235",
            price : "$200",
            img : "./src/assets/images/black_elegant_leather_jacket-120x156.jpg"
          },
          {
            name: "Leather Gloves",
            star: 5,
            author: "by Beardman",
            img : "./src/assets/images/leather_gloves-120x156.jpg"
          },
          {
            name: "Hipster Black Top",
            titlePrice: "$57",
            img : "./src/assets/images/hipster_black_top-120x156.jpg"
          },
          {
            name: "Modern Leather Boots",
            titlePrice : "$50",
            price: "$30",
            img : "./src/assets/images/brown_dress_shoes-200x260.jpg"
          },
          {
            name: "Spring Printed Dress",
            star: 5,
            price : "$47",
            img : "./src/assets/images/spring_printed_dress-120x156.jpg"
          },
          {
            name: "Spring Printed Dress",
            star: 5,
            author: "by admin",
            img : "./src/assets/images/spring_printed_dress-120x156.jpg"
         }
        ]
      }
    }
   }
</script>

<template>
   <!--container generale-->
   <div class="container-fluid summaryH">
      <hr class="mx-5">

      <!--titoli delle sezioni-->
      <div class="row row-cols-4 paddingRowSummary">
         <div v-for="title in titles" :key="title" class="col d-flex justify-content-start align-items-center">
            <h5>{{title}}</h5>
         </div>
      </div>

      <!--contenitore prodotti-->
      <div class="row row-cols-4 paddingRowSummary w-100">
         <div v-for="product in products" :key="product" class="col d-flex align-items-center p-3">
            <div class="d-flex prodBorder productContainer w-100 justify-content-between">
               <div class="d-flex flex-column">

                  <!--descrizione prodotto-->
                  <p>
                     <span>{{ product.name }}</span>
                     <span :class="product.price != null ? 'text-decoration-line-through' : ''">{{ product.titlePrice }}</span>
                  </p>
                  <div class="d-flex mb-3">
                     <i class="fa-sharp fa-solid fa-star theme" v-for="i in product.star" :key="i"></i>
                  </div>

                  <!--uso di un ternario per determinare se i prezzi sono sottolineati o meno e quando lo sono-->
                  <p>
                     <span class="text-decoration-line-through">{{ product.sales}}</span>
                     <span :class="product.sales != null || product.titlePrice != null ? 'text-decoration-underline' : ''">{{ product.price }}</span>
                     <span>{{ product.author }}</span>
                  </p>
               </div>
               <div class="d-flex">
                  <img class="summaryImg" :src="product.img" alt="">
               </div>
            </div>
         </div>
      </div>
   </div>
</template>

<style class="scss">
   .summaryH{
      height: 515px;
   }
   .summaryImg{
      width: 60px;
      height: 78px;
   }
   .prodBorder{
    padding-top: 15px;
    border-bottom: 1px solid #35383c;
  }
  .paddingRowSummary{
   padding: 0px 400px;
  }
  .productContainer{
   height: 120px;
  }
</style>