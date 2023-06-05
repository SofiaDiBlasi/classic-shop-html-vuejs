<script>
   export default {
    name: "FeaturedProducts",

    data(){
      return {
         //creo un array di oggetti con tutte le info per i prodotti       
        featuredProduct: [ {
          type: "Men",  
          capo: [
            { img: "./src/assets/images/black_elegant_leather_jacket-200x260.jpg",
              testo1: "Black Leather Jacket",    
              testo2: "Men,Jackets,Jeans",
              prezzoSbarrato: "$235",
              prezzo: "$200" 
            },
            { img: "./src/assets/images/black_leather_suit-200x260.jpg",
              testo1: "Black Leather Suit",    
              testo2: "Men,Jackets",
              prezzo: "$176" 
            },
            { img: "./src/assets/images/blue_jacket_and_white_stripe_tee-200x260.jpg",
              testo1: "Black Leather & Stripe Tee",    
              testo2: "Men,Jackets,Suits",
              prezzo: "$580"  

            },
            { img: "./src/assets/images/modern_black_leather_suit-200x260.jpg",
              testo1: "Modern Black Leather Suit",    
              testo2: "Men,Jackets",
              prezzo: "$96"  
            }
          ]
          }, 
          { 
            type: "Women",  
            capo: [
              { img: "./src/assets/images/black_leather_jacket-200x260.jpg",
                testo1: "Black Leather Jacket",    
                testo2: "Women,Jackets",
                prezzoSbarrato: "$400",
                prezzo: "$200" 
              },
              { img: "./src/assets/images/hipster_black_top-200x260.jpg",
                testo1: "Hipster Black top",    
                testo2: "Women,Top",
                prezzo: "$106" 
              },
              { img: "./src/assets/images/modern_love_tee-200x260.jpg",
                testo1: "Modern Love Tee",    
                testo2: "Men,T-Shirt",
                prezzoSbarrato: "$350",
                prezzo: "$280"  

              },
              { img: "./src/assets/images/spring_printed_dress-200x260.jpg",
                testo1: "Spring Printed Dress",    
                testo2: "Women,Dress",
                prezzo: "$180"  
              }
            ]
          },
          { 
            type: "Accessories",  
            capo: [
              { img: "./src/assets/images/leather_gloves-200x260.jpg",
                testo1: "Leather Gloves",    
                testo2: "Gloves",
                prezzo: "$145" 
              },
              { img: "./src/assets/images/brown_dress_shoes-200x260.jpg",
                testo1: "Brown Dress Shoes",    
                testo2: "Shoes",
                prezzoSbarrato: "$470",
                prezzo: "$350" 
              }
            ]
          }
        ],
        //creo una variabile che farà da counter al metodo che faremo dopo per switchare le sezioni, messa in posizione 0 per prendere il primo elemento dell'array
        currentButton : 
        {
          type: "Men",  
          capo: [
            { img: "./src/assets/images/black_elegant_leather_jacket-200x260.jpg",
              testo1: "Black Leather Jacket",    
              testo2: "Men,Jackets,Jeans",
              prezzoSbarrato: "$235",
              prezzo: "$200" 
            },
            { img: "./src/assets/images/black_leather_suit-200x260.jpg",
              testo1: "Black Leather Suit",    
              testo2: "Men,Jackets",
              prezzo: "$176" 
            },
            { img: "./src/assets/images/blue_jacket_and_white_stripe_tee-200x260.jpg",
              testo1: "Black Leather & Stripe Tee",    
              testo2: "Men,Jackets,Suits",
              prezzo: "$580"  

            },
            { img: "./src/assets/images/modern_black_leather_suit-200x260.jpg",
              testo1: "Modern Black Leather Suit",    
              testo2: "Men,Jackets",
              prezzo: "$96"  
            }
          ]
        }
      }
    },
    methods: {
      changeCategoria (event) {
        this.currentButton = this.featuredProduct[event.currentTarget.value]; 
      }
    },
  }
</script>

<template>
  <!--contenitore generale-->
  <div  class="container-fluid px-0 featuredBox mb-5">
    <!--titolo-->
    <div class="row h-30 justify-content-center align-items-center">
      <div class="col-3"><hr class="mb-5" /></div>
      <div class="col-auto text-center">
        <h1>Featured Products</h1>
        <p>Must have products from our top sellers</p>
      </div>
      <div class="col-3"><hr class="mb-5"/></div>
    </div>
    <!--bottoni categorie-->
    <div class="row h-20 justify-content-center align-items-center">
      <div class="btn-group w-30 mb-5" role="group">
        <button class="categoriaButton btn" @click="changeCategoria($event)" v-for="categoria in featuredProduct" :key="categoria" :value="featuredProduct.indexOf(categoria)">{{categoria.type}}</button>
      </div>
    </div> 
    <!--immagini-->
    <div class="row h-50 justify-content-center align-items-center product-container">
      <div class="col-auto d-flex flex-column align-items-center justify-content-center" v-for="card in currentButton.capo" :key="card">
        <div>
          <img class="productImg" :src="card.img" alt="">
          <p>{{ card.testo1 }}</p>
          <small>{{ card.testo2 }}</small>
          <p class="d-flex theme"><span class="text-decoration-line-through" :class="card.prezzoSbarrato != null ? 'd-block':'d-none'">{{ card.prezzoSbarrato }}</span>{{ card.prezzo }}</p>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss">
   @import "../style.scss";

  .featuredBox {
    height: 700px;
  }
  .categoriaButton {
    color: black !important;
    background-color: lightgray !important;
    border: 1px solid lightgray !important;
    width: 100px !important;
    height: 50px !important;

    &:hover{
      background-color: white;
    }
    &:focus {
      background-color: white !important;
  }
}
  .productImg{
    width: 200px;
    height: 260px;
  }

  .w-30{
    width: 30%!important;
  }
  .product-container {
    padding: 0 250px;
  }

  .theme{
    color: $mainTheme;
  }
</style>