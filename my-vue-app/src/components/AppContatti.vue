<script>
   export default {
    name: "Terms",

    data() {
      return {
        avadaInfo : [
          "12345 North Main Street,",
          "New York, NY 555555",
          "Phone: 1.800.555.6789",
          "Email:info@company.com",
          "Web:Theme-fusion.com"
        ],
        iconeSocial : [
              "fa-brands fa-facebook-f",
              "fa-brands fa-twitter",
              "fa-brands fa-instagram",
              "fa-brands fa-youtube"
        ],
        products : [
          {
            name: "Leather Gloves",
            price : "$45",
            img : "./src/assets/images/leather_gloves-120x156.jpg"
          },
          {
            name: "Black Leather Jacket",
            sales: "$235",
            price : "$200",
            img : "./src/assets/images/black_elegant_leather_jacket-120x156.jpg"
          },
          {
            name: "Spring Printed Dress",
            price : "$47",
            img : "./src/assets/images/spring_printed_dress-120x156.jpg"
          }
        ],
        post : [
        "> a aaaaaaaaaaaaaaaaa a aaaaaaaaa a ",
        "> aaaa aaa aaaaaaaaa aaaa   aaaaaaaaa ",
        "> aaaaaaa aaaaaaa aa aaa a aa aa aaaaa ",
        "> aaaaaaaaaaa   aaaaaaaaaaaaaaaaaa ",
        "> aaaaaaaaaaa aaaaaa aa aaaaaaaaaa ",
        "> aaaaaaaaa aaaa  aaaaaa aaaaaaaaaa "
       ],
        tags : [
          "Black",
          "boots",
          "Brown",
          "Casual",
          "D&G",
          "fabric",
          "flowers",
          "Grey",
          "hat",
          "Hipster",
          "lines",
          "multi-purpose",
          "New York",
          "Outdoors",
          "red",
          "responsive",
          "summer",
          "sweater",
          "Travel",
          "Warm",
          "White",
          "winter"
       ],
       
      }
    }
  }
</script>

<template>
    <div class="container-fluid secContainer pt-5">

      <!--avada info-->
      <div class="row h-100 justify-content-center">

        <div class="col-2 h-100 d-flex flex-column justify-content-start">
          <!--logo-->
          <img class="mb-5" src="../assets/images/classic_shop_logo_footer.png" alt="">
          <!--contatti-->
          <p class="text-white" v-for="info in avadaInfo" :key="info" >{{ info }}</p>
          <!--icone social-->
          <div class="mt-5">
            <i v-for="icone in iconeSocial" :key="icone" :class="icone" class="m-2 text-white"></i>
          </div>
        </div>

        <!--top prod-->
        <div class="col-2 h-100 d-flex flex-column justify-content-start align-items-start ms-5">
          <h5 class="text-white">TOP RATED PRODUCTS</h5>
          <div class="d-flex justify-content-between w-100 prodBorder" v-for="product in products" :key="product">
             <div class="d-flex flex-column text-white">
                <p>{{ product.name }}</p>
                <div class="d-flex mb-3">
                  <i class="fa-sharp fa-solid fa-star text-primary" v-for="i in 5" :key="i"></i>
                </div>
                <p>{{ product.price }}</p>
              </div>
             <div class="d-flex">
                <img class="footerImg" :src="product.img" alt="">
             </div>
          </div>
        </div>

        <!--posts-->
        <div class="col-2 h-100 d-flex flex-column justify-content-start align-items-start">
          <h5 class="text-white">RECENT POSTS</h5>
          <div class="link text-white" v-for="link in post" :key="link">
            {{ link }}
          </div>
        </div>

        <!--tags-->
        <div class="col-2 h-100 d-flex flex-column justify-content-start align-items-start">
          <h5 class="text-white">TAGS</h5>
          <div class="d-flex flex-wrap">
            <p v-for="tag in tags" :key="tag" class="text-white tag fw-bold">{{ tag }}</p>
          </div>
        </div>
      </div>
    </div>
</template>

<style lang="scss">
  .secContainer{
    background-color: #2b2e32;
    height: 500px;
  }
  .tag {
    border: 1px solid #35383c;
    padding: 5px 9px;
    margin: 2px;
  }
  .link {
    padding: 15px 0px;
    border-bottom: 1px solid #35383c;
  }
  .prodBorder{
    padding-top: 15px;
    border-bottom: 1px solid #35383c;
  }
  .footerImg{
    width: 60px;
    height: 78px;
  }
</style>
