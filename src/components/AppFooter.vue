<script>
import AppBanner from "./AppBanner.vue"
import footerMenu from "../footerMenu"

export default{
   name: "AppFooter",
   components: {
      AppBanner,
   },
   data () {
      return {
         footerMenu,
      }
   },

}
</script>

<template>
   <footer>
      <AppBanner></AppBanner>

      <div class="site-map">
         <div class="container py-5 d-flex justify-content-between overflow-hidden">

            <!-- Left Side Site Map -->
            <div class="footer-menu d-flex flex-column flex-wrap">
               
               <div v-for="footerItem in footerMenu" class="me-3 mb-3">
                  <a href="#" class="site-map-page">{{ footerItem.name }}</a>
                  <div class="d-flex flex-column align-items-start">
                     <a v-for="footerVoice in footerItem.voices" href="#" class="site-map-sub">{{ footerVoice }}</a>
                  </div>
               </div>

            </div>
               

            <!-- Right Side Logo -->
            <img src="../assets/img/dc-logo-bg.png">
         </div>
         
      </div>

      <div class="lower-footer">
         <div class="container py-4 d-flex justify-content-between">
            
            <button class="btn">Sign-up now!</button>

            <div class="d-flex align-items-center">
               <a href="#" class="me-3">Follow Us</a>
               <div class="social">
                  <a href="#" class="me-3"><img src="../assets/img/footer-facebook.png"></a>
                  <a href="#" class="me-3"><img src="../assets/img/footer-twitter.png"></a>
                  <a href="#" class="me-3"><img src="../assets/img/footer-youtube.png"></a>
                  <a href="#" class="me-3"><img src="../assets/img/footer-pinterest.png"></a>
                  <a href="#"><img src="../assets/img/footer-periscope.png"></a>
               </div>
            </div>
         
         </div>

      </div>
   
   </footer>
</template>
