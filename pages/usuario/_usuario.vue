<template>
  <b-container>
    <div id="perfil">
        <b-avatar class="img"></b-avatar>
        <h1>{{ usuario.nome }}</h1>
        <p>{{ usuario.email }}</p>
        <p>{{ usuario.senha }}</p>
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