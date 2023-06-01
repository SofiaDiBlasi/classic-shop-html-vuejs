<script>
   export default {
    name: "BigBanner",

    data(){
      return{

        //creo un counter
        counter : 0,

        //creo una array con le url delle immagini che mi servono
        bannerSlider: [
          "./src/assets/images/home1_slide_one_bg.jpg",
          "./src/assets/images/home1_slide_2_bg.jpg",
          "./src/assets/images/home1_slide_three_bg_2.jpg"
        ],

        //creo una variabile che avrà come valore la prima img, o il set interval partirebbe vuoto
        currentBanner : "./src/assets/images/home1_slide_one_bg.jpg",
      }
    },

    //creo un metodo per fare in modo che ogni 2 secondi cambi il bg del mio dv
    methods: {
      sliderBanner() {
        //all'inizio del set Interval creo un if, in moto tale che il counter si resetti una volta arrivato a 3, valore massimo dell'array
        setInterval(() => {
          if (this.counter==3) {
            this.counter = 0
          }
          this.currentBanner = this.bannerSlider[this.counter];
          this.counter++;
        }, 2000);
      }
    },
    //con un mounted vado a chiamarmi il metodo dell'intervallo di tempo
    mounted() {
      this.sliderBanner();
    }
  }
</script>

<template>

  <!--contenitore generale-->
  <div :style="'background-image: url(' + currentBanner + '); background-size: cover'" class="container-fluid bigBanner px-0">
    <div class="row align-items-center justify-content-center h-100">
      <div class="col-auto d-flex flex-column justify-content-center align-items-center h-100">

        <!--testo del banner-->
        <h1 class="text-light">Brand New Arrivals</h1>
        <p class="text-light">NEW COLLECTION FROM NEW YORK</p>

        <!--pulsanti-->
        <div class="d-flex">
          <button class="btn btn-lg bannerBtn text-light rounded-pill mx-2 px-4">VIEW ALL</button>
          <button class="btn btn-lg bannerBtn text-light rounded-pill mx-2 px-4">LOOKBOOK</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  .bigBanner{
    height: 600px;
  }
  .bannerBtn {
    background-color:rgba(255, 255, 255, 0.1) !important;
    border: 1px solid white !important;
    color: white !important;
  }
</style>