<template lang="pug">
  div.navApp
    b-navbar(toggleable="sm" variant="primary" type="dark")
      b-navbar-nav
        b-nav-item {{ nomeCidade }}
      b-navbar-nav.ml-auto
        b-nav-item Home
        b-nav-item Diversão
        b-nav-item Sua turma
        b-nav-item Promoções
        b-nav-item Ajuda
      b-navbar-nav.ml-auto
        b-nav-item Notificação
</template>
<script>
export default {
  name: 'AppHeader',
  data () {
    return {
      nomeCidade: 'Belo Horizonte - MG'
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
