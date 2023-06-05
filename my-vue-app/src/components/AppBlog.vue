<script>
   export default {
    name: "Blog",

    data() {
      return {
         blogPost : [
            {
               img: "./src/assets/images/post_img_12-700x441.jpg",
               titolo: "Aenean lobortis sapien enim viverra",
               data: "September 9th, 2015 | ",
               commenti: "0 Comments",
               testo: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla."
            },
            {
               img: "./src/assets/images/post_img_11-700x441.jpg",
               titolo: "Duis ac massa semper maximus",
               data: "September 9th, 2015 | ",
               commenti: "0 Comments",
               testo: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla."
            },
            {
               img: "./src/assets/images/post_img_10-700x441.jpg",
               titolo: "Nunc fermit nulla eu justo sem id",
               data: "September 9th, 2015 | ",
               commenti: "0 Comments",
               testo: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla."
            }
         ]
      }
    }
   }
</script>

<template>

   <!--contenitore generale-->
   <div class="container-fluid blogBox">

      <!--titolo-->
      <div class="row h-30 justify-content-center align-items-center">
         <div class="col-3"><hr class="mb-5" /></div>
         <div class="col-auto text-center">
            <h1>From Our Blog</h1>
            <p>The latest Classic Shop news</p>
         </div>
         <div class="col-3"><hr class="mb-5"/></div>
      </div>

      <!--img e testo-->
      <div class="row blogCard h-70 justify-content-center align-items-center">
         <div class="col d-flex flex-wrap flex-column justify-content-center align-items-start p-0" v-for="post in blogPost" :key="post">
            <img class="blogImg" :src="post.img" alt="">
            <h5>{{ post.titolo }}</h5>
            <small>{{ post.data }} {{ post.commenti }}</small>
            <p>{{ post.testo }}</p>
         </div>
      </div>
      
   </div>
</template>

<style lang="scss">
   .blogBox{
      height: 720px;
   }
   .blogCard{
      padding: 10px 170px;
   }
   .blogImg{
      height: 315px;
      width: 500px;
   }
</style>
