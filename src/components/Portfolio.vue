<template>
  <div class="portfolio">
    <h3>Portfolio</h3>
    <div class="portfolio-grid">
      <div class="portfolio-item">
        <a href="">
          <img src="../assets/logo_copel.svg" alt="Copel">
        </a>    
      </div>
       <div class="portfolio-item">
         <a href="">
          <img src="../assets/herospark.png" alt="Herospark">
        </a>     
      </div>
       <div class="portfolio-item">
         <a href="">
          <img src="../assets/eadbox.png" alt="EADBOX">
        </a>     
      </div>
       <div class="portfolio-item">
         <a href="">
          <img src="../assets/starsoft.png" alt="Starsoft">
        </a>     
      </div>
      <div class="portfolio-item">
        <a href="">
          <img src="../assets/aftersale.png" alt="Aftersale">
        </a>     
      </div>
      <div class="portfolio-item">
        <a href="">
         <img src="../assets/gilson.png" alt="Gilson Coelho">
        </a>     
      </div>
      <div class="portfolio-item">
        <a href="">
         <img src="../assets/likluc.webp" alt="Likluc">
        </a>     
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Portfolio'
}
</script>

<style scoped>
.portfolio {
  height: 86vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: linear-gradient(rgba(255,255,255,0.99), rgba(255,255,255,0.95)), url('../assets/desktop.svg');
  background-repeat: no-repeat;
  background-size: contain;
}
@media(max-width: 992px) {
  .portfolio {
    height: auto;
  }
}
.portfolio-grid {
  display: grid;
  justify-content: center;
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
  grid-gap: 15px;
  grid-template-columns: repeat(auto-fit, 200px);
  margin-top: 20px;
}
.portfolio-item img{
  height: 60px;
  width: 100%;
  object-fit: contain;
  margin: 10px;
  transition: 0.3s all;
}
.portfolio-item img:hover{
  transform: scale(1.1);
}
</style>
