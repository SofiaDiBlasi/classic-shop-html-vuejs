<script>
   export default {
    name: "NavBar",

    data() {
      return {
        iconeSocial : [
              "fa-brands fa-facebook-f",
              "fa-brands fa-twitter",
              "fa-brands fa-instagram",
              "fa-brands fa-youtube"
        ],
        accountInfo : [
              "Profilo",
              "Impostazioni",
              "Disconnetti",
              "Contatta Assistenza"
        ],
        cartItem : [
            "n-1 T-shirt Tg Sx",
            "n-2 Cappello in lana"
        ],
        navMenù : [
            "Home",
            "Shop",
            "Products",
            "Categories",
            "News",
            "Elements"
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
  <div class="d-flex flex-column w-100">

    <!--sezione 1-->

    <!--parte alta header-->
    <div class="cart container row">

      <!--parte sinistra-->

      <!--icone social-->
      <div class="col-6">
        <i v-for="icone in iconeSocial" :key="icone" :class="icone" class="iconeSocial m-2"></i>
      </div>

      <!--parte destra-->

      <div class="col-6">
        <div class="row m-0 p-0">

          <!--shopping cart-->
          <div class="offset-2 col-2 m-2 p-0">
            Shopping Cart
          </div>

          <!--menù profilo-->
          <select id="cartItem" class="col-2 dropdown m-2 p-0 border-0" aria-label="Default select example">
            <option>
               My Account
            </option>
            <option v-for="info in accountInfo" :key="info" :value="info">{{ info }}</option>
          </select>

          <!--menù carrello-->
            <select id="cartItem" class="col-2 dropdown m-2 border-0" aria-label="Default select example">
              <option>
                <span class="cartIcon">&#xf07a;</span>
                Cart</option>
              <option v-for="item in cartItem" :key="item" :value="item">{{ item }}</option>
            </select>
        </div>
      </div>
    </div>

    <hr class="my-0">

    <!--sezione 2-->

    <!--parte bassa header-->

    <!--logo Avada-->
    <div class="row m-0">
      <div class="col-2">
        <img src="../assets/images/classic_shop_logo1x.png" alt="">
      </div>

      <!--select menù navbar-->
      <select v-for="navSection in navMenù" :key="navSection" class="col-1 dropdown m-2 navBar py-0 my-0" aria-label="Default select example">
        <option>{{ navSection }}</option>
        <option v-for="navItem in navItem" :key="navItem" :value="navItem">{{ navItem }}</option>
      </select>

          <!--shop button-->
      <div class="col-3">
        <a class="btn btn-primary rounded-pill" href="#" role="button">SHOP NOW!</a>
      </div>

      <!--search bar o solo icona? chiedere-->
      <div></div>

    </div>
  </div>
</template>

<style lang="scss">
  .cart {
    height: 3.5rem;
  }

  .iconeSocial{
    color: #494949;
  }

  .navBar{
    color: #494949;
    border: none;
    height: 100px;
    &:hover {
      color: blue;
      border-top: 1px solid blue;
    }
  }
  
  select { 
    font-family: "Font Awesome\ 5 Free" !important; 
    font-weight: 900; 
  }
</style>