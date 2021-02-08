<template>
  <div class="portfolio">
    <h3>Portfolio</h3>
    <div class="portfolio-grid">
      <div class="portfolio-item">
        <a href="">
          <img src="../assets/logo_copel.svg" alt="">
        </a>    
      </div>
       <div class="portfolio-item">
         <a href="">
          <img src="../assets/herospark.png" alt="">
        </a>     
      </div>
       <div class="portfolio-item">
         <a href="">
          <img src="../assets/eadbox.png" alt="">
        </a>     
      </div>
       <div class="portfolio-item">
         <a href="">
          <img src="../assets/starsoft.png" alt="">
        </a>     
      </div>
      <div class="portfolio-item">
        <a href="">
          <img src="../assets/aftersale.png" alt="">
        </a>     
      </div>
      <div class="portfolio-item">
        <a href="">
         <img src="../assets/gilson.png" alt="">
        </a>     
      </div>
      <div class="portfolio-item">
        <a href="">
         <img src="../assets/likluc.webp" alt="">
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
  height: 87vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
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
h3 {
  color: #1a0e33;
  font-size: 43px;
  z-index: 99;
  margin-top: 95px;
}
.portfolio-item img{
  height: 60px;
  width: 100%;
  object-fit: contain;
  margin: 10px;
}
</style>
