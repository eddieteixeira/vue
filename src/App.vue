<template>
  <div id="app">
    <Header :activeTab="activeTab"/>
    <Hero v-if="activeTab === 'Hero'" heroTitle="Desenvolvimento de aplicativos e websites" />
    <Atuacao v-if="activeTab === 'Atuacao'" atuacaoText="Soluções"/>

  </div>
</template>
<script>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Atuacao from './components/Atuacao.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    Atuacao
  },
 data() {
   return {
     activeTab: 'Hero'
   }
 }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Source+Code+Pro:wght@900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap');
body {
 margin: 0;
 background-color: #ffffff;
 width: 100%;
 overflow-x: hidden;
}
#app {
  font-family: 'Source Code Pro', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1a0e33;
}
p, a, ul, li, span, a {
  font-family: 'Roboto', sans-serif;
  font-weight: normal;
}
</style>
