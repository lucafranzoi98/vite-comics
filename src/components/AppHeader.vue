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
      <nav class="m-auto dc_max_width d-flex justify-content-between align-items-center">
         <a href="#">
            <img src="../assets/img/dc-logo.png" alt="DC" width="70">
         </a>
           
         <div class="h-100 d-flex">
            <div v-for="item in navBarMenu" class="h-100 d-flex align-items-center ms-3 position-relative">
               <a href="#" :class="(item.active ? 'active-page-navbar' : '')">
                  {{ item.name.toUpperCase() }}
               </a>
            </div>            
         </div>
      </nav>  

   </header>

</template>