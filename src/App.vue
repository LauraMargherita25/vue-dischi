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

<style lang="scss" scoped>
@import "./assets/styles/style.scss";

#app {
  background-color: $blue_bg;
}
</style>

