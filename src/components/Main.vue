<template>
  <div class="main">
    <Contact />
    <!-- Navbar -->
    <div class="header">
      <div class="header-content">

        <a @click="activeTab= 'Hero'">
          <h1>Eddie Teixeira</h1>
        </a>

          <img class="mobileMenu" 
          src="../assets/menu.svg" 
          alt="Menu"
          v-if="mobile === false"
          :class="{ active: mobile }" @click="mobile = !mobile">

        <ul class="deskMenu" v-if="mobile === false">
          <li><a @click="activeTab= 'Atuacao'">atuação</a></li>
          <li><a @click="activeTab= 'Portfolio'">portfolio</a></li>
          <li><a @click="activeTab= 'Sobre'">sobre</a></li>
          <li><a @click="activeTab= 'Atuacao'">contato</a></li>
        </ul>
          <ul class="deskMenuMob" v-if="mobile === true">
          <li><a @click="activeTab= 'Atuacao'">atuação</a></li>
          <li><a @click="activeTab= 'Portfolio'">portfolio</a></li>
          <li><a @click="activeTab= 'Sobre'">sobre</a></li>
          <li><a @click="activeTab= 'Atuacao'">contato</a></li>
        </ul>
        <img class="mobileClose" 
          @click="mobile = !mobile"
          src="../assets/close.svg" 
          v-if="mobile === true"
        >
      </div>
    </div>
    <!-- Components -->
    <div class="components">
      <Hero v-if="activeTab === 'Hero'" heroTitle="Desenvolvimento de aplicativos e websites"/>
      <Atuacao v-if="activeTab === 'Atuacao'" />
      <Portfolio v-if="activeTab === 'Portfolio'" />
      <Sobre v-if="activeTab === 'Sobre'"/>
    </div>
  </div>
</template>

<script>
import Hero from './Hero.vue';
import Atuacao from './Atuacao.vue';
import Portfolio from './Portfolio.vue';
import Sobre from './Sobre.vue';
import Contact from './Contact.vue';
export default {
  name: 'Main',
  components: {
    Hero,
    Atuacao,
    Portfolio,
    Sobre,
    Contact
  },
  data() {
    return {
      activeTab: 'Hero',
      mobile: false
    }
  }
}

</script>

<style scoped>
.components {
  padding: 45px 20px 20px 20px;
}
.header {
  width: 100%;
  background-color: #009cff;
  /* position: fixed; */
  z-index: 999;
  border-bottom: 6px solid #1a0e33
}
.header-content {
  max-width: 1200px;
  display: inline-flex;
  width: 100%;
  justify-content: space-around;
  align-items: center;
}
.mobileMenu,
.mobileClose {
  max-width: 20px;
  margin: 0 20px;
  transition: 0.2s all;
}
.mobileMenu:hover,
.mobileClose:hover {
  filter: invert(1);
  cursor: pointer;
}
.deskMenuMob {
  display: none;
}
@media(min-width: 992px) {
  .mobileMenu,
  .mobileClose {
    display: none;
  }
}
@media(max-width: 992px) {
  .deskMenu {
    margin: 20px 40px;
    display: flex;
    flex-direction: column;
    display: none;
  }
  .deskMenuMob {
    display: flex;
    flex-direction: column;
  }
  .deskMenuMob li {
    margin: 10px 0;
  }
}
h1 {
  color: #1a0e33;
  font-family: 'Source Code Pro', monospace;
  font-size: 20px;
  font-weight: 700;
  text-align: left;
  transition: 0.3s all;
}
h1:hover{
  color: #fff;
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
