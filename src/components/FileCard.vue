<template>
  <div class="col">
    <div class="album_card p-3 text-center">
      <img :src="albumData.poster" :alt="albumData.title" class="img-fluid">
      <h1 class="text-uppercase fw-bold text-light">{{ albumData.title }}</h1>
      <h2>{{ albumData.genre }}</h2>
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
  background-color: $blue_card;
}
</style>