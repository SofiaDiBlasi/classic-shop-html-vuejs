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
  <div :style="'background-image: url(' + currentBanner + ')'" class="container-fluid">
    <div class="row">
      <div class="col bigBanner d-flex flex-column justify-content-center align-items-center my-0 py-0">

        <!--testo del banner-->
        <h1 class="text-light">Brand New Arrivals</h1>
        <h5 class="text-light">NEW COLLECTION FROM NEW YORK</h5>

        <!--pulsanti-->
        <div class="d-flex">
          <button class="bannerBtn text-light rounded-pill">VIEW ALL</button>
          <button class="bannerBtn text-light rounded-pill">LOOKBOOK</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  .bigBanner{
    width: 100%;
    height: 600px;
  }
  .bannerBtn {
    background-color:rgba(255, 255, 255, 0.3);
    border: 1px solid white;
  }
</style>