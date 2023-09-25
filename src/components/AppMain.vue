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
         <div class="row dc_max_width m-auto py-5">

            <AppComic v-for="comic in comics.comics" :name=comic.series :img=comic.thumb></AppComic>

         </div>
      </div>
   </main>
   

</template>
