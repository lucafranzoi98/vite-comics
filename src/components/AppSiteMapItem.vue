<script>
export default{
   name: "AppSiteMapItem",
   props: {
      name: String,
      voices: Array
   }

}
</script>

<template>

   <div class="me-5 mb-3">
      <a href="#" class="site-map-page">{{ name }}</a>
      <div class="d-flex flex-column align-items-start mt-2">
         <a v-for="voice in voices" href="#" class="site-map-sub">{{ voice }}</a>
      </div>
   </div>

</template>