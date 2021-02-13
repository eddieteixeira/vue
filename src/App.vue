<template>
  <div class="app-eddie">
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
.app-eddie {
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
h3 {
  color: #1a0e33;
  font-size: 43px;
  z-index: 99;
  /* margin-top: 95px; */
}
</style>
