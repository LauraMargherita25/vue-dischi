<template>
    <div id="app">
      <file-header @search="searchRilevato"/>
      <file-main :search-string = "strSearch"/>
    </div>
</template>

<script>
import FileHeader from './components/FileHeader.vue'
import FileMain from './components/FileMain.vue'

export default {
  name: 'App',
  components: {
    FileHeader,
    FileMain
  },
  data() {
    return {
      strSearch: "",
    }
  },
  methods: {
    searchRilevato(strSearch) {
      console.log("sono il cl di app" + strSearch);
      this.strSearch = strSearch;
    }
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "./assets/styles/style.scss";
#app{
  width: 100%;
  height: 100%;
}
</style>

