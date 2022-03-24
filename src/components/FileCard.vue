<template>
  <div class="col">
    <div class="album_card p-3 text-center">
      <img src=	"https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="" class="img-fluid">
      <h1 class="text-uppercase fw-bold text-light">Titolo</h1>
      <h2>Autore</h2>
      <p>Anno</p>
    </div>
  </div>
</template>

<script>
export default {
    name: "FileCard"
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables.scss";
.album_card{
  background-color: $blue_card;
}
</style>