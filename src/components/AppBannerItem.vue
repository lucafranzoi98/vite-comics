<script>
export default{
   name: "AppBannerItem",
   props: {
      img: String,
      name: String
   }
}
</script>

<template>

   <div class="d-flex align-items-center">
      <img :src="img" class="me-3" :height="name == 'DC power visa' ? '30' : '50'">
      <span class="text-white text-uppercase">{{name}}</span>
   </div>

</template>