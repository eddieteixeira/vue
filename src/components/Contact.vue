<template>
  <div class="contact">
    <img src="../assets/coffee.svg" alt="">
  </div>
</template>

<script>
export default {
  name: 'Contact'
}
</script>

<style scoped>
.contact {
  position: fixed;
  z-index: 90;
  bottom: 0;
  right: 0;
  margin: 20px;
  padding: 12px;
  border-radius: 50%;
  box-shadow: 1px 1px 6px rgba(0,0,0,0.4);
  transition: 0.4s all;
  animation: floating 3s ease-in-out infinite
}
.contact img {
  width: 40px;
  height: 100%;
  fill: #009cff;
  opacity: 0.7;
}
.contact:hover{
  transform: scale(1.1);
  cursor: pointer;
  opacity: 0.5;
}

</style>
