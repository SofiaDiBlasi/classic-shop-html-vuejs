<script>
   export default {
    name: "NavBar",

    data() {
      return {
        socialIcon : [
              "fa-brands fa-facebook-f",
              "fa-brands fa-twitter",
              "fa-brands fa-instagram",
              "fa-brands fa-youtube"
        ],
        navMenù : [
          {
            name:"Home",
            order:0
          },
          {
            name:"Shop",
            order:1
          },
          {
            name:"Products",
            order:2
          },
          {
            name:"Categories",
            order:3
          },
          {
            name:"Elements",
            order:5
          }
        ],
        navItem : [
            "opzione 1",
            "opzione 2",
            "opzione 3",
            "opzione 4",
            "opzione 5",
            "opzione 6"
        ]
      }
    }
  }
</script>

<template>

  <!--contenitore generale-->
  <div class="container-fluid header-container px-0">

    <!--sezione 1-->

    <!--parte alta header-->
    <div class="row align-items-center h-30">

      <!--parte sinistra-->

      <!--icone social-->
      <div class="col-6 text-center">
        <i v-for="icon in socialIcon" :key="icon" :class="icon" class="iconeSocial mx-3"></i>
      </div>

      <!--parte destra-->

      <div class="col-6 h-100">
        <div class="row h-100">

          <!--shopping cart-->
          <div class="d-flex flex-row-reverse col-3 border-end h-100 align-items-center">
            <div>Shopping Cart</div>
          </div>

          <!--menù profilo-->
          <div class="d-flex col-2 border-end h-100 align-items-center">
            <button class="btn dropdown-toggle" type="button" data-toggle="dropdown" aria-expanded="false">
              My Account
            </button>
          </div>

          <!--menù carrello-->
          <div class="d-flex col-3 bg-light h-100 align-items-center">
            <button class="btn dropdown-toggle" type="button" data-toggle="dropdown" aria-expanded="false">
              <i class="fa-solid fa-cart-shopping"></i>
              CART
            </button>
          </div>
        </div>
      </div>
    </div>

    <hr class="m-0">

    <!--sezione 2-->

    <!--parte bassa header-->

    <!--logo Avada-->
    <div class="row h-70">
      <div class="offset-2 col-2 logo text-center h-100 align-items-center justify-content-center d-flex">
        <img src="../assets/images/classic_shop_logo1x.png" alt="">
      </div>

      <!--select menù navbar-->
      <div class="offset-1 col-7 select text-center h-100 align-items-center d-flex">
        <div class="dropdown">
            <button v-for="voce in navMenù" :key="voce" :class="'order-'+ voce.order" class="navBar rounded-0 btn dropdown-toggle h-100" type="button" data-bs-toggle="dropdown" aria-expanded="false">
              {{ voce.name }}
            </button>
            <ul class="dropdown-menu">
              <li v-for="item in navItem" :key="item" class="dropdown-item">
                {{item}}
              </li> 
            </ul>
        </div>
        
        <!--bottone solo per News-->
        <button class="navBar h-100 rounded-0 btn order-4" href="">News</button>
        <!--bttone shop now + ricerca-->
        <button type="button" class="avadaButton btn text-white btn-lg rounded-pill font-weight-bold mx-5 px-4 order-6">
          SHOP NOW!
        </button>
        <!--bottone in hover-->
        <button type="button" class="avadaHover d-none btn text-white btn-lg rounded-pill font-weight-bold mx-5 px-4 order-6">
          GET AVADA NOW!
        </button>
        <i class="fa-solid fa-magnifying-glass fs-6 ms-1 order-7"></i>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  @import "../style.scss";

  .header-container {
    font-size: 15px !important;
    height: 140px;
  }
  .h-30 {
    height: 30%;
  }
  .h-70 {
    height: 70%;
  }
  .btn {
    font-size: 15px !important;
  }
  .avadaButton{
    display: block;
    background-color: $mainTheme !important;

    &:hover {
      display: none;
    }
  }
  .avadaButton:hover ~ .avadaHover {
    display:block !important;
    background-color: $secondaryTheme !important;
  }
  .iconeSocial{
    color: #494949;
  }
  .navBar{
    color: #494949;
    border: none;
    &:hover {
      color: $mainTheme !important;
      border-top: 1px solid $mainTheme !important;
    }
  }
  select { 
    font-family: "Font Awesome\ 5 Free" !important; 
    font-weight: 900; 
  }
  .order-6 {
    order: 6 !important;
    }
  .order-7 {
      order: 7 !important;
    }  
</style>