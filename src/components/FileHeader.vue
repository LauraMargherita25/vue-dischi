<template>
  <header class="mb-5">
      <div class="container-fluid d-flex">
        <a class="navbar-brand" href="#">
            <img src="../../public/img/spotify_logo.png" alt="" class="img-fluid">
        </a>
        <p class="text-light">{{ stringaRicerca }}</p>
        <file-serch-components @search="setSearchGenre"/>
      </div>
  </header>
</template>

<script>
import FileSerchComponents from './FileSerchComponents.vue';

export default {
  name: "FileHeader",
  data() {
      return {
          stringaRicerca: ""
      }
  },
  methods: {
      setSearchGenre(genereAlbum) {
          this.stringaRicerca == genereAlbum,
          console.log(genereAlbum)
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
    .navbar-brand{
        width: 80px;
    }
}
</style>