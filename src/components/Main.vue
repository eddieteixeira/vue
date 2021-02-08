<template>
  <div class="main">
    <!-- Navbar -->
    <div class="header">
      <div class="header-content">
        <a @click="activeTab= 'Hero'">
          <h1>Eddie Teixeira</h1>
        </a>
        <ul>
          <li><a @click="activeTab= 'Hero'">soluções</a></li>
          <li><a @click="activeTab= 'Atuacao'">portfolio</a></li>
          <li><a @click="activeTab= 'Atuacao'">sobre</a></li>
          <li><a @click="activeTab= 'Atuacao'">contato</a></li>
        </ul>
      </div>
    </div>
    <!-- Components -->
    <div class="components">
      <Hero v-if="activeTab === 'Hero'" heroTitle="Desenvolvimento de aplicativos e websites"/>
      <Atuacao v-if="activeTab === 'Atuacao'" />
    </div>
  </div>
</template>

<script>
import Hero from './Hero.vue';
import Atuacao from './Atuacao.vue';
export default {
  name: 'Main',
  components: {
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

<style scoped>
.components {
  padding-top: 45px;
}
.header {
  width: 100%;
  background-color: #009cff;
  position: fixed;
  z-index: 999;
  border-bottom: 10px solid #1a0e33
}
.header-content {
  max-width: 1200px;
  display: inline-flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
h1 {
  color: #1a0e33;
  font-family: 'Source Code Pro', monospace;
  font-size: 20px;
  font-weight: 700;
  text-align: left;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  /* margin: 0 10px; */
}
a {
  color: #1a0e33;
  text-decoration: none;
  font-weight: bold;
  padding: 5px 10px;
  transition: 0.3s all;
}
a:hover {
  border-radius: 4px;
  color: #fff;
  cursor: pointer;
}
</style>
