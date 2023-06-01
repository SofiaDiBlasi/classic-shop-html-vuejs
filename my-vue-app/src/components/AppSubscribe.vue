<script>
   export default {
    name: "Subscribe"
   }
</script>

<template>
   <div class="sub container-fluid">
      <div class="row h-100 justify-content-center align-items-center">
         <div class="col-5 d-flex justify-content-center align-items-center">
               <div class="mailBox d-flex justify-content-center align-items-center mx-3">
                 <i class="fa-sharp fa-regular fa-envelope text-white"></i> 
               </div>
               <h4 class="text-white my-0">Subscribe now and get special offers</h4>
         </div>

         <!--mail form-->
         <div class="col-4 d-flex justify-content-center align-items-center">
            <form class="d-flex justify-content-center align-items-center">
               <div class="form-group mx-sm-3 mb-2">
                  <input type="email" class="form-control rounded-pill inputMail" id="exampleFormControlInput1" placeholder="Insert your mail">
               </div>
               <button type="submit" class="btn btn-primary mb-2 rounded-pill px-5">SEND</button>
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
   .mailBox{
      height: 30px;
      width: 30px;
      background-color: #2b2e32;
      border-radius: 50%;
   }
   .inputMail{
      width: 300px !important;
   }
</style>