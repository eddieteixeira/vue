<template>
  <div class="sobre">
    <h3>Sobre</h3>
    <div class="sobre-flex">
      <div class="sobre-img">
        <img src="../assets/eddie.jpg" alt="">
      </div> 
      <div class="sobre-text">
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sunt delectus in voluptate mollitia quam, optio perferendis omnis ipsam! Aspernatur non ipsum enim consequuntur quos vero explicabo minus nesciunt dolorem ratione?</p>
       </div> 
    </div>
  </div>
</template>

<script>
export default {
  name: 'Sobre'
}
</script>

<style scoped>
.sobre {
  height: 87vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: linear-gradient(rgba(255,255,255,0.99), rgba(255,255,255,0.95)), url('../assets/connect.svg');
  background-repeat: no-repeat;
  background-size: contain;
}
@media(max-width: 992px) {
  .sobre {
    height: auto;
  }
}
.sobre-flex {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  max-width: 1200px;
  margin: 45px auto;
}
@media(max-width: 992px) {
  .sobre-flex {
    flex-direction: column;
  }
}
.sobre-img {
  width: 30%;
  padding: 20px;
}
.sobre-text {
  width: 70%;
  padding: 20px;
}
@media(max-width: 992px) {
  .sobre-img, 
  .sobre-text {
    width: 100%;
  }
}
.sobre-img img {
  border-radius: 50%;
  max-width: 250px;
  border: 5px solid rgba(0,0,0,0.07);
}
.sobre-text {
  text-align: left;
}
</style>
