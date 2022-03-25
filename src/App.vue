<template>
    <div id="app">
      <file-header/>
      <file-main/>
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

