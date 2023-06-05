<script>
   export default {
    name: "Contatti"
  }
</script>

<template>
  <!--contenitore generale-->
  <div class="container-fluid paymentBg pt-5">

    <!--testo copyright-->
    <div class="row h-30 text-center">
      <div class="col">
        <h6 class="col-auto text-white copyrightText">©Copyright 2012-2020 | Avada theme by Theme Fusion | All Rights reserved | Powered by WordPress</h6>
      </div>
    </div>

    <!--img pagamenti-->
    <div class="row h-70">
      <div class="col d-flex justify-content-center align-items-center">
        <img class="paymentImg" src="../assets/images/payment_cards_footer.png">
      </div>
    </div>

  </div>
</template>

<style lang="scss">
  .paymentBg{
    height: 150px;
    background-color: #1d1f22;
  }
  .paymentImg{
    height: 40px;
    width: 400px;
  }
  .copyrightText{
    font-size: 13px;
  }
</style>