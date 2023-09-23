<script>
export default{
   name: "AppHeader",
   data () {
      return {
         navItems: [
            "Characters", "Comics", "Movies", "Tv", "Games", "Collectibles", "Videos", "Fans", "News", "Shop"
         ]
      }
   },
}
</script>

<template>

   <header>
      <nav class="navbar m-auto py-3">
         <div>
            <a class="navbar-brand" href="#">
               <img src="../assets/img/dc-logo.png" alt="DC" width="50">
            </a>
         </div>
            
         <div>
            <a href="#" v-for="navItem in navItems" class="ms-4">{{ navItem.toUpperCase() }}</a>
         </div>
      </nav>   
   </header>

</template>

<style lang="scss" scoped>

</style>