<script>
   export default{
    name: "Testimonial",
    
   }
</script>

<template>

   <!--contenitore generale-->
   <div class="container-fluid testimonialBox">

      <!--base template importato-->
      <div id="carouselExampleIndicators" class="carousel slide h-80 w-100" data-bs-ride="true">

         <!--bottoni-->
         <div class="carousel-indicators">
            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active dots" aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2" class="dots"></button>
         </div>

         <!--testo e img 1-->
         <div class="carousel-inner h-100 w-100">
            <div class="carousel-item active h-100 w-100">
               <div class="d-flex flex-column justify-content-center align-items-center h-100 textBox">
                  <img src="/src/assets/images/man_testimonial.png" alt="">
                  <p class="text-white">Curabitur non tristique tortor. Vestibulum aliquet suscipit in volutpat. Donec vel lacinia sem, vitae semper nulla. In hac habitasse platea dictumst. Mauris consectetur est et nibh sadip hendrerit bibendum.</p>
                  <p class="text-white">Darìo Pineda, Theme Fusion</p>
               </div>
            </div>

            <!--testo e img 2-->
            <div class="carousel-item h-100 w-100">
               <div class="d-flex flex-column justify-content-center align-items-center h-100 textBox">
                  <img src="/src/assets/images/woman_testimonial.png" alt="">
                  <p class="text-white">Curabitur non tristique tortor. Vestibulum aliquet suscipit in volutpat. Donec vel lacinia sem, vitae semper nulla. In hac habitasse platea dictumst. Mauris consectetur est et nibh sadip hendrerit bibendum.</p>
                  <p class="text-white">Paola Pippa, Theme Fusion</p>
               </div>
            </div>
         </div>

      </div>
   </div>
</template>

<style class="scss">
   .testimonialBox {
      height: 550px;
      background-image: url(../assets/images/testimonials_home_1_bg.jpg);
      background-size: cover;
      background-repeat: no-repeat;
   }
   .dots{
      width: 20px !important;
      height: 20px !important;
      border-radius: 50%;
   }
   .textBox{
      padding: 0px 500px;
   }
</style>