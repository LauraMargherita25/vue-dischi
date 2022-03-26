<template>
  <header class="mb-5">
      <div class="container-fluid d-flex p-1 align-items-center">
        <a class="me-auto" href="#">
            <img src="../../public/img/spotify_logo.png" alt="" class="img-fluid">
        </a>
        <file-serch-components @search="setSearchGenre"/>
      </div>
  </header>
</template>

<script>
import FileSerchComponents from './FileSerchComponents.vue';

export default {
  name: "FileHeader",
  methods: {
      setSearchGenre(genereAlbum) {
        this.$emit('search', genereAlbum);
        console.log("sono il cl di header" + genereAlbum); 
      }
  },
  components:{
      FileSerchComponents
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables.scss";
header{
    background-color: $blue_header;
    a{
        width: 80px;
    }
}
</style>