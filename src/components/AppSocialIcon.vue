<script>
export default{
   name: "AppSocialIcon",
   props: {
      img: String
   }
}
</script>

<template>

   <a href="#" class="me-3">
      <img :src="img">
   </a>

</template>