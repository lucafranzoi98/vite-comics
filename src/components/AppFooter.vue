<script>
import AppBanner from "./AppBanner.vue"

export default{
   name: "AppFooter",
   components: {
      AppBanner,
   },
   data () {
      return {
         navItems: [
            "Characters", "Comics", "Movies", "Tv", "Games", "Videos", "News",
         ]
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
            <div class="d-flex">

               <!-- First Column -->
               <div class="me-4">
                  <div>
                     <a href="#" class="site-map-page">
                        Dc comics
                     </a>
                     <div class="site-map-sub d-flex flex-column mt-2 mb-3">
                        <a href="#" v-for="navItem in navItems">{{ navItem }}</a>
                     </div>
                  </div>
                  <div>
                     <a href="#" class="site-map-page">
                        Shop
                     </a>
                     <div class="site-map-sub d-flex flex-column mt-2">
                        <a href="#">Shop DC</a>
                        <a href="#">Shop DC Collectibles</a>
                     </div>
                  </div>
               </div>
               
               <!-- Second Column -->
               <div class="me-4">
                  <div>
                     <a href="#" class="site-map-page">
                        DC
                     </a>
                     <div class="site-map-sub d-flex flex-column mt-2">
                        <a href="#">Terms Of Use</a>
                        <a href="#">Privacy Policy (new)</a>
                        <a href="#">Ad Choices</a>
                        <a href="#">Advertising</a>
                        <a href="#">Jobs</a>
                        <a href="#">Subscriptions</a>
                        <a href="#">Talent Workshops</a>
                        <a href="#">CPSC Certificates</a>
                        <a href="#">Ratings</a>
                        <a href="#">Shop Help</a>
                        <a href="#">Contact Us</a>
                     </div>
                  </div>
               </div>

               <!-- Third Column -->
               <div>
                  <div>
                     <a href="#" class="site-map-page">
                        Sites
                     </a>
                     <div class="site-map-sub d-flex flex-column mt-2">
                        <a href="#">DC</a>
                        <a href="#">MAD Magazine</a>
                        <a href="#">DC Kids</a>
                        <a href="#">DC Universe</a>
                        <a href="#">DC Power Visa</a>
                     </div>
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
                  <a href="#"><img src="../assets/img/footer-facebook.png" class="me-3"></a>
                  <a href="#"><img src="../assets/img/footer-twitter.png" class="me-3"></a>
                  <a href="#"><img src="../assets/img/footer-youtube.png" class="me-3"></a>
                  <a href="#"><img src="../assets/img/footer-pinterest.png" class="me-3"></a>
                  <a href="#"><img src="../assets/img/footer-periscope.png"></a>
               </div>
            </div>
         
         </div>

      </div>
   
   </footer>
</template>
