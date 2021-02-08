<template>
  <div class="atuacao">
    <h3>Atuação</h3>
    <div class="atuacao-grid">
      <div class="atuacao-item">
        <img src="../assets/web-icon.png" alt="">
        <a>Websites</a>
        <p class="hidden">
          WEBSITES Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam facilis amet officia quidem at dolor delectus eum vitae temporibus impedit? Nobis reprehenderit fuga dignissimos doloremque vel, necessitatibus hic expedita earum.
        </p>
      </div>
       <div class="atuacao-item">
        <img src="../assets/mobile.png" alt="">
        <a>Aplicativos</a>
          <p class="hidden">
          APLICATIVOS Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam facilis amet officia quidem at dolor delectus eum vitae temporibus impedit? Nobis reprehenderit fuga dignissimos doloremque vel, necessitatibus hic expedita earum.
        </p>
      </div>
       <div class="atuacao-item">
        <img src="../assets/otimizacao-icon.png" alt="">
        <a>Landing pages</a>
        <p class="hidden">
          LPS Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam facilis amet officia quidem at dolor delectus eum vitae temporibus impedit? Nobis reprehenderit fuga dignissimos doloremque vel, necessitatibus hic expedita earum.
        </p>
      </div>
       <div class="atuacao-item">
        <img src="../assets/dev-icon.png" alt="">
        <a>Outros</a>
        <p class="hidden">
          OUTROS Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam facilis amet officia quidem at dolor delectus eum vitae temporibus impedit? Nobis reprehenderit fuga dignissimos doloremque vel, necessitatibus hic expedita earum.
        </p>
      </div>
    </div>
    <div class="atuacao-content">

    </div>
  </div>
</template>

<script>
export default {
  name: 'Atuacao',
  props: {
    atuacaoText: String,
  }
}
</script>

<style scoped>
.hidden {
  display: none;
}
.atuacao-grid {
  display: grid;
  justify-content: center;
  width: 100%;
  grid-gap: 15px;
  grid-template-columns: repeat(auto-fit, 400px);
  margin-top: 20px;
}
.atuacao-item {
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 1px 1px 6px rgba(0,0,0,0.4);
  border-radius: 5px;
}
.atuacao-item:hover{
  box-shadow: 1px 1px 10px rgba(0,0,0,0.4);
  cursor: pointer;
}
.atuacao-item:hover a{
  color: #009cff;
}
h3 {
  font-size: 43px;
  z-index: 99;
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
   margin: 10px;
}

</style>
