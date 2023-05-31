<script>
   export default {
    name: "Subscribe"
   }
</script>

<template>
   <div class="sub container-fluid">
      <div class="row">
         <div class="col-6">
            <div class="col-3">
               <i class="fa-sharp fa-regular fa-envelope text-white"></i>
            </div>
            <div class="col-3">
               <h5 class="text-white">Subscribe now and get special offers</h5>
            </div>
         </div>

         <!--mail form-->
         <div class="col-6">
            <form class="form-inline">
                  <div class="form-group mx-sm-3 mb-2">
                  <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Insert your mail">
               </div>
               <button type="submit" class="btn btn-primary mb-2">SEND</button>
               </form>
         </div>
      </div>
   </div>
</template>

<style lang="scss">
   .sub{
      background-color: #303337;
      height: 235px;
   }
</style>