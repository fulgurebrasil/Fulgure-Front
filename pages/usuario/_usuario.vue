<template>
  <b-container>
    <div id="perfil">
      <b-avatar class="img"></b-avatar>
      <h1>{{ usuario.nome }}</h1>
      <p>{{ usuario.email }}</p>
      <p>{{ usuario.senha }}</p>
      <b-button v-on:click="deletaUsuario">Clique</b-button>
      <h1 id="delete"></h1>
    </div>
    <div id="lixeira"></div>
  </b-container>
</template>

<script>
export default {
  async asyncData({ $axios, route }) {
    const idUsuario = route.params.usuario
    const resposta = await $axios.get('/usuario/' + idUsuario)
    const usuario = resposta.data
    return { usuario }
  },
  methods: {
    deletaUsuario() {
      const id = this.$route.params.usuario
      this.$axios.delete('/usuario/' + id)
    },
  },
}
</script>

<style>
#perfil {
  border-radius: 10px;
  margin-bottom: 20px;
  width: 85%;
  margin: auto;
  box-shadow: 3px 3px 3px 3px #9b9b9b;
}
</style>