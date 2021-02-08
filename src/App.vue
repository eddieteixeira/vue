<template>
  <div class="app">
    <Main />
  </div>
</template>

<script>
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Main
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&family=Source+Code+Pro:wght@700&display=swap');
body {
  margin: 0;
  overflow-x: hidden;
}
.app {
  font-family: 'Source Code Pro', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
}

p, a, ul, li, span {
  font-family: 'Roboto', sans-serif;
}
</style>
