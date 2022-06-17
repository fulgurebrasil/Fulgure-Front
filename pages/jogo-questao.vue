<template>
  <div>
    <b-container>
      <menuHamburguer></menuHamburguer>
      <b-button class="vidas" type="button">
        <img src="../static/coracao2.png" />
        <span>3</span>
      </b-button>

      <b-button class="timer" type="button">
        <span>00:30</span>
        <img src="../static/relogio.png" />
      </b-button>
      <b-container id="containerDica">
        <h1>Dica
          <img src="../static/iconFechar.png" @click="showDica" />

        </h1>
        <b-container class="conteudoDica">
          <p>A região norte tem como pratos característicos a mandioca, o açaí, o feijão, o peixe e a rapadura.
          </p>
          <p>Você possui 9 dicas restantes.</p>
        </b-container>
      </b-container>
      <dicaQuestao class="dicaTxt"></dicaQuestao>

      <h1 class="identificador">Questão {{ questoes.id }}</h1>
      <b-container class="questao">
        <p>
          {{ questoes.comando }}
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
          <b-button class="dica" @click="showDica">
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
  head: {
    title: 'Questão 1',
    link: [
      {
        rel: 'preconnect',
        href: 'https://fonts.googleapis.com',
      },
      {
        rel: 'preconnect',
        href: 'https://fonts.gstatic.com',
      },
      {
        rel: 'stylesheet',
        href: 'https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap',
      },
    ],
  },
  data() {
    return {
      questoes: {
        id: 1,
        comando: 'Qual a maior influência cultural na culinária nortista brasileira?',
      }
    }
  },
  methods: {
    showDica() {
      const dica = document.getElementById('containerDica');
      if (dica.style.display === 'block') {
        dica.style.display = 'none'
      } else {
        dica.style.display = 'block'
      }
    }
  }
}
</script>

<style>
body {
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
}

.dicaTxt {
  margin-top: 30px;
  display: none;
}

.vidas {
  width: 80px;
  height: 40px;
  border-radius: 37px;
  color: white;
  display: inline-block;
  flex-direction: left;
  background-color: #345fcd;
  border: none;
  box-shadow: 2px 2px 2px #c4c4c4;
  font-weight: bolder;
}

.vidas img {
  width: 26px;
  height: 20px;
}

.timer {
  background-color: transparent;
  border: none;
  color: black;
  width: 125px;
  height: 50px;
  border-radius: 37px;
  float: right;
  font-weight: bolder;
  font-size: 22px;
}

.timer img {
  width: 30px;
  height: 28px;
}

.timer:hover {
  background-color: transparent;
  color: black;
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
  font-size: 14px;
  font-weight: bolder;
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
  font-weight: bolder;
  text-align: center;
  color: white;
  margin-top: 10%;
  margin-bottom: 10px;
  padding: 4px 0;
}

.questao p {
  color: black;
  margin-top: 0;
}

.botoes {
  margin-top: 60px;
  display: flex;
  justify-content: center;
}

.responder {
  margin: 0 auto;
  margin-top: 50px;
}

.centralizar {
  margin-left: 5%;
  margin-right: 5%;
}

.alternativa {
  display: block;
}

.dica:hover,
.pular:hover {
  background-color: #ffc700;
}

.vidas:hover {
  background-color: #345fcd;
}

.responder:hover {
  background-color: #3d9a8a;
}

#containerDica {
  z-index: 3;
  display: none;
  margin-top: 20px;
}

#containerDica h1,
.conteudoDica {
  box-shadow: 3px 3px 3px #9b9b9b;
  border-radius: 6px;
}

#containerDica h1 {
  background-color: black;
  font-size: 30px;
  font-weight: bolder;
  text-align: center;
  color: white;
  padding: 4px 0;
  margin-bottom: 5px;
}

.conteudoDica {
  color: black;
  margin-top: 0;
}

#containerDica h1 img {
  cursor: pointer;
  width: 27px;
  height: 27px;
  border-radius: 50%;
  display: block;
  float: right;
  margin-right: 5px;
}
</style>