<script>
import AppBanner from "./AppBanner.vue"
import footerMenu from "../footerMenu.js"
import AppSiteMapItem from "./AppSiteMapItem.vue"
import AppSocialIcon from "./AppSocialIcon.vue"
import socialIcon from "../socialIcon.js"

export default{
   name: "AppFooter",
   components: {
      AppBanner,
      AppSiteMapItem,
      AppSocialIcon
   },
   data () {
      return {
         footerMenu,
         socialIcon
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

   <footer>

      <!-- Blue Banner -->
      <AppBanner></AppBanner>

      <div class="site-map">
         <div class="pt-5 d-flex justify-content-between overflow-hidden dc_max_width m-auto">

            <!-- Left Side: Site Map -->
            <div class="footer-menu d-flex flex-column flex-wrap">
               
               <AppSiteMapItem v-for="item in footerMenu" :name="item.name" :voices="item.voices"></AppSiteMapItem>

            </div>
               

            <!-- Right Side: Logo -->
            <img src="../assets/img/dc-logo-bg.png">
         </div>
         
      </div>

      <div class="lower-footer">

         <div class="py-4 d-flex justify-content-between dc_max_width m-auto">
            
            <button>Sign-up now!</button>

            <div class="d-flex align-items-center">
               <a href="#" class="me-3">Follow Us</a>

               <AppSocialIcon v-for="item in socialIcon" :img=getImagePath(item.img)></AppSocialIcon>
               
            </div>
         
         </div>

      </div>
   
   </footer>
</template>
