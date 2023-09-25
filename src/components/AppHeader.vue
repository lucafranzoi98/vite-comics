<script>
import navBarMenu from "../navBarMenu"
export default{
   name: "AppHeader",
   data () {
      return {
         navBarMenu
      }
   },
}
</script>

<template>

   <header>
      <nav class="navbar m-auto py-3 dc_max_width">
         <a class="navbar-brand" href="#">
            <img src="../assets/img/dc-logo.png" alt="DC" width="50">
         </a>
           
         <div>
            <a href="#" v-for="navBarItem in navBarMenu" class="ms-4">
               {{ navBarItem.toUpperCase() }}
            </a>
         </div>
      </nav>  

   </header>

</template>