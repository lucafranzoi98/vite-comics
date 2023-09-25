<script>
import bannerItems from "../bannerItems.js"
import AppBannerItem from "./AppBannerItem.vue";

export default{
   name: "AppBanner",
   components: {
      AppBannerItem
   },
   data (){
      return{
         bannerItems
      }
   },
   methods: {
      getImagePath: function(img) {
         return new URL (`../assets/img/${img}`, import.meta.url).href;
      }
   }
}
</script>

<template>

   <div class="banner">

      <div class="container py-5 d-flex justify-content-around dc_max_width">

         <AppBannerItem v-for="item in bannerItems" :name=item.name :img=getImagePath(item.img)></AppBannerItem>
         
      </div>

   </div>

</template>