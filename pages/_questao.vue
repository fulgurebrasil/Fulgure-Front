<template>
  <div>
    <b-container>
      <menuHamburguer></menuHamburguer>
      <b-button class="vidas" type="button">
        <img src="../static/coracao.png" />
        <span>3</span>
      </b-button>

      <b-button class="timer" type="button">
        <span>00:30</span>
        <img src="../static/relogio.png" />
      </b-button>
      <div class="identificador">Questão 1</div>
      <b-container class="questao">
        <p>
          Qual a maior influência cultural na culinária nortista brasileira?
        </p>
        <b-form-radio-group id="grupo1">
          <b-form-radio class="alternativa">Europeia</b-form-radio>
          <b-form-radio class="alternativa">Norte-Americana</b-form-radio>
          <b-form-radio class="alternativa">Indígena</b-form-radio>
          <b-form-radio class="alternativa">Asiática</b-form-radio>
          <b-form-radio class="alternativa">Australiana</b-form-radio>
          <span></span>
        </b-form-radio-group>
      </b-container>
      <b-button-toolbar class="botoes">
          <b-button class="voltar">
            <img src="../static/voltar.png" />
          </b-button>
          <b-button-group class="centralizar">
            <b-button class="dica">
              Dica
              <img src="../static/lampada.PNG" />
            </b-button>
            <b-button class="pular">
              Pular
              <img src="../static/coracaoPartido.PNG" />
            </b-button>
          </b-button-group>
          <b-button class="avancar">
            <img src="../static/avancar.png" />
          </b-button>
        </b-button-toolbar>
        <b-button class="responder">
          Responder
          <img src="../static/seta.PNG" />
        </b-button>
    </b-container>
  </div>
</template>

<script>
import menuHamburguer from '~/components/menuHamburguer.vue'
export default {
  components: { menuHamburguer },
}
</script>

<style>
.vidas {
  width: 100px;
  height: 40px;
  border-radius: 37px;
  color: white;
  display: inline-block;
  flex-direction: left;
  background-color: #345fcd;
}
.vidas img {
  width: 26px;
  height: 23px;
}
.timer {
  background-color: transparent;
  border: none;
  color: black;
  width: 100px;
  height: 40px;
  border-radius: 37px;
  float: right;
}
.timer img {
  width: 30px;
  height: 28px;
}
.questao,
.identificador {
  box-shadow: 3px 3px 3px #9b9b9b;
  border-radius: 6px;
}
.voltar,
.avancar {
  background-color: transparent;
  border: none;
}
.voltar img,
.avancar img {
  width: 25px;
  height: 35px;
}
.dica,
.pular {
  font-weight: bold;
  color: black;
  background-color: #ffc700;
  width: 85px;
  height: 41px;
  border-radius: 37px;
  border: none;
  box-shadow: 2px 2px 2px #c4c4c4;
}
.dica img {
  height: 21px;
  width: 20px;
}
.pular {
  width: 90px;
}
.pular img {
  height: 14px;
  width: 18px;
}
.responder {
  font-weight: bold;
  color: white;
  background-color: #3d9a8a;
  width: 150px;
  height: 41px;
  border-radius: 37px;
  display: block;
  flex-direction: center;
  border: none;
}
.responder img {
  width: 21px;
  height: 19px;
}
.botoes {
  width: 100%;
}
.identificador {
  background-color: black;
  font-size: 30px;
  font-weight: bold;
  text-align: center;
  color: white;
  margin-top: 10%;
  margin-bottom: 10px;
}
.questao p {
  color: black;
  margin-top: 0;
}
.botoes{
    margin-top: 60px;
    display: flex;
    justify-content: center;
}
.responder{
    margin: 0 auto;
    margin-top: 100px;
}
.centralizar{
    margin-left: 5%;
    margin-right: 5%;
}
.alternativa{
    display: block;
}
.dica:hover, .pular:hover{
    background-color: #ffc700;
}
.vidas:hover{
    background-color: #345fcd;
}
.responder:hover{
    background-color: #3d9a8a;
}
</style>