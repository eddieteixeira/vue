<template>
  <div class="hero">
    <div class="hero-text">
      <h2>{{ heroTitle }}</h2>
    </div>
    <div class="hero-img">
      <img src="../assets/hero.png" alt="">
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hero {
  height: 90vh;
  padding: 20px;
  display: inline-flex;
  width: 100%;
  max-width: 1400px;
  justify-content: space-around;
  align-items: center;
}
@media(max-width: 992px) {
  .hero {
    height: auto;
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
    font-size: 40px;
  }
}

.hero-img {
  height: 100%;
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
@media(max-width: 992px) {
  .hero-img {
    width: 100%;
  }
}
.hero-img img {
  width: 100%;
  height: auto;
  -webkit-filter: drop-shadow(5px 5px 5px rgba(0,0,0,0.1));
  filter: drop-shadow(5px 5px 5px rgba(0,0,0,0.1));
}
</style>
