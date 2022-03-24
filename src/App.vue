<template>
    <div id="app">
      <file-main/>
    </div>
</template>

<script>
import FileMain from './components/FileMain.vue'

export default {
  name: 'App',
  components: {
    FileMain
  }
}
</script>

<style lang="scss">
@import "./assets/styles/style.scss";

#app {
}
</style>

