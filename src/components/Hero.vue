<template>
  <div class="hero">
    <div class="hero-text">
      <h2>{{ heroTitle }}</h2>
    </div>
    <div class="hero-img">
      <img src="../assets/hero1-2.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    heroTitle: String,
  }
}
</script>

<style scoped>
.hero {
  height: 82vh;
  padding: 20px;
  display: inline-flex;
  width: 100%;
  max-width: 1400px;
  justify-content: space-around;
  align-items: center;
  background: linear-gradient(rgba(255,255,255,0.99), rgba(255,255,255,0.95)), url('../assets/code.svg');
  background-repeat: no-repeat;
  background-size: cover;
}
@media(max-width: 992px) {
  .hero {
    height: auto;
    margin: 20px;
    width: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
.hero-text {
  width: 50%;
}
@media(max-width: 992px) {
  .hero-text {
    margin-top: 45px;
    width: 100%;
  }
}
h2 {
  color: #1a0e33;
  font-size: 70px;
  text-align: left;
  white-space: break-spaces;
}
@media(max-width: 992px) {
  h2 {
    font-size: 8vw;
  }
}

.hero-img {
  height: 100%;
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  background-image: url('../assets/hero2-2.png');
  background-size: 100%;
  background-position: center;
  background-repeat: no-repeat;
}
@media(max-width: 992px) {
  .hero-img {
    width: 100%;
  }
}

.floating {   
    animation-name: floating; 
    animation-duration: 3s; 
    animation-iteration-count: infinite; 
    animation-timing-function: ease-in-out; 
    margin-left: 30px; 
    margin-top: 5px; 
} 
  
@keyframes floating { 
    0% { transform: translate(0,  0px); } 
    50%  { transform: translate(0, 10px); } 
    100%   { transform: translate(0, -0px); }     
} 

.hero-img img {
  width: 100%;
  height: auto;
  -webkit-filter: drop-shadow(5px 5px 5px rgba(0,0,0,0.1));
  filter: drop-shadow(5px 5px 5px rgba(0,0,0,0.1));
  transition: 0.4s;
  animation: floating 3s ease-in-out infinite
}

</style>
