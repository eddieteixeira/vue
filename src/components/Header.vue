<template>
  <div class="header">
    <div class="header-content">
      <a href="/">
        <h1>Eddie Teixeira</h1>
      </a>
      <ul>
        <li><a href="" @click="activeTab= 'Hero'">soluções</a></li>
        <li><a href="" @click="activeTab= 'Atuacao'">portfolio</a></li>
        <li><a href="" @click="activeTab= 'Atuacao'">sobre</a></li>
        <li><a href="" @click="activeTab= 'Atuacao'">contato</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    activeTab: {
      type: String,
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  width: 100%;
  background-color: #009cff;
  position: fixed;
  z-index: 999;
}
.header-content {
  max-width: 1200px;
  display: inline-flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
h1 {
  color: #fff;
  font-size: 20px;
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
  color: #fff;
  text-decoration: none;
  padding: 5px 10px;
  transition: 0.3s all;
}
a:hover {
  border-radius: 4px;
  color: #1a0e33;
  font-weight: bold;
}
</style>
