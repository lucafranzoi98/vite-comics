<script>
   export default{
      name: "AppComic",
      props: {
         img: String,
         name: String
      }
   }
</script>

<template>

   <div class="col-2 mb-3 p-2">
      <a href="#" class="comic-thumb mb-2">
         <img :src="img" class="w-100">
      </a>      
      <a href="#" class="text-white text-uppercase comic-series">{{name}}</a>
   </div>

</template>