<template>
  <div class="atuacao">
    <h3>Atuação</h3>
    <div class="atuacao-grid">
      <div class="atuacao-item" @click="activeTab='websites'">
        <img src="../assets/web.svg" alt="">
        <a>Websites</a>
      </div>
       <div class="atuacao-item" @click="activeTab='aplicativos'">
        <img src="../assets/phone.svg" alt="">
        <a>Aplicativos</a>
      </div>
       <div class="atuacao-item" @click="activeTab='lp'">
        <img src="../assets/funnel.svg" alt="">
        <a>Landing pages</a>
      </div>
       <div class="atuacao-item" @click="activeTab='outros'">
        <img src="../assets/code.svg" alt="">
        <a>Outros</a>
      </div>
    </div>
    <div class="atuacao-content">
      <p v-if="activeTab === 'websites' ">
        WEBSITES Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam facilis amet officia quidem at dolor delectus eum vitae temporibus impedit? Nobis reprehenderit fuga dignissimos doloremque vel, necessitatibus hic expedita earum.
      </p>
      <p v-if="activeTab === 'aplicativos' ">
        APLICATIVOS Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam facilis amet officia quidem at dolor delectus eum vitae temporibus impedit? Nobis reprehenderit fuga dignissimos doloremque vel, necessitatibus hic expedita earum.
      </p>
      <p v-if="activeTab === 'lp' ">
        LPS Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam facilis amet officia quidem at dolor delectus eum vitae temporibus impedit? Nobis reprehenderit fuga dignissimos doloremque vel, necessitatibus hic expedita earum.
      </p>
      <p v-if="activeTab === 'outros' ">
        OUTROS Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam facilis amet officia quidem at dolor delectus eum vitae temporibus impedit? Nobis reprehenderit fuga dignissimos doloremque vel, necessitatibus hic expedita earum.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Atuacao',
  props: {
    atuacaoText: String,
  },
  data() {
    return { 
      activeTab: 'websites'
    }
  }
}
</script>

<style scoped>
.hidden {
  display: none;
}
.atuacao {
  height: 86vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: linear-gradient(rgba(255,255,255,0.99), rgba(255,255,255,0.92)), url('../assets/terminal.svg');
  background-repeat: no-repeat;
  background-size: contain;
}
@media(max-width: 992px) {
  .atuacao {
    height: auto;
  }
}
.atuacao-grid {
  display: grid;
  justify-content: center;
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
  grid-gap: 15px;
  grid-template-columns: repeat(auto-fit, 200px);
  margin-top: 20px;
}
.atuacao-item {
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 1px 1px 6px rgba(0,0,0,0.4);
  background-color: #fff;
  border-radius: 5px;
  transition: 0.2s all;
}
.atuacao-item:hover{
  box-shadow: 1px 1px 10px rgba(0,0,0,0.4);
  cursor: pointer;
  background: #009cff;
  margin-top: -5px;
}
.atuacao-item:hover a{
  color: #fff;
}
.atuacao-item:hover img{
  filter: invert(1);
}
a {
  color: #464646;
  font-weight: bold;
}
.atuacao-img {
  position: absolute;
  top: -90px;
  left: 90px;
  max-width: 200px;
}
.atuacao-item img{
   max-width: 70px;
   max-height: 60px;
   margin: 10px;
   opacity: 0.8;;
}
.atuacao-content {
  margin: 45px auto;
  max-width: 800px;
  text-align: left;
  font-size: 18px;
  line-height: 1.6em;
}
</style>
