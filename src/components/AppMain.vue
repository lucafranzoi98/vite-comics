<script>
import AppComic from './AppComic.vue';
import comics from "../comics.js"

export default{
   name: "AppMain",
   data (){
      return {
         comics
      }
   },
   components: {
      AppComic,
   }
}
</script>

<template>

   <main>
      <div class="upper-main">
         <div class="text-uppercase dc_max_width m-auto position-relative h-100">
            <div class="badge-jumbotron">Current series</div>
         </div>
         
      </div>
      <div class="lower-main">
         <div class="dc_max_width m-auto py-5">

            <div class="row">
               <AppComic v-for="comic in comics.comics" :name=comic.series :img=comic.thumb></AppComic>
            </div>

            
            <div class="d-flex justify-content-center">
               <a href="#" class="text-white px-5 py-2 load-more-btn text-uppercase">Load more</a>
            </div>
            
         </div>

         
      </div>
   </main>
   

</template>
