<template>
  <div class="col mb-5">
    <div class="album_card p-3 text-center">
      <div class="img_wrapper mb-3">
        <img :src="albumData.poster" :alt="albumData.title" >
      </div>
      <p class="text-uppercase text-light fw-bold fs-4">{{ albumData.title }}</p>
      <p class="fs-5 mb-0">{{ albumData.genre }}</p>
      <p>{{ albumData.year }}</p>
    </div>
  </div>
</template>

<script>
export default {
    name: "FileCard",
    props: {
      albumData: Object
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables.scss";
.album_card{
  height: 380px;
  background-color: $blue_card;
  color: $text_color;
  .img_wrapper{
    width: 160px;
    height: 160px;
    img{
      width: 100%;
      object-fit: cover;
    }
  }
}
</style>