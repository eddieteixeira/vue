<script>
export default {
  name: 'Atuacao',
  props: {
    atuacaoText: String,
  },
    render(createElement) {
    return createElement('div', {class:'atuacao'} ,[
      createElement('div', {class:'border-top'}),
      createElement('div', {class:'atuacao-text'}, [
        createElement('h3', {}, 'Atuação')
      ]),
      createElement('div', {class:'atuacao-grid'}, [
        createElement('div', {class: 'atuacao'}, [
          createElement('h4', {}, 'Websites e aplicações')
        ]),
        createElement('div', {class: 'atuacao'}, [
          createElement('h4', {}, 'Websites e aplicações')
        ]),
        createElement('div', {class: 'atuacao'}, [
          createElement('h4', {}, 'Websites e aplicações')
        ]),
        createElement('div', {class: 'atuacao'}, [
          createElement('h4', {}, 'Websites e aplicações')
        ])
      ])
    ])
  }
}
</script>

<style scoped>
.atuacao {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
}
h3 {
  font-size: 43px;
  z-index: 99;
}
.border-top {
  width: 100%;
  max-width: 150px;
  border: 3px solid #009cff;
}
.atuacao-img {
  position: absolute;
  top: -90px;
  left: 90px;
  max-width: 200px;
}
.atuacao-text {
  background-color: #fff;
  padding: 50px;
  width: 60%;
  height: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.atuacao-grid {
  display: grid;
  justify-content: center;
  width: 100%;
  grid-gap: 15px;
  grid-template-columns: repeat(auto-fit, 400px);
}
.atuacao img{
   max-width: 90px;
}

</style>
