<template lang="pug">
  div.navApp
    b-navbar(toggleable="sm" variant="primary" type="dark")
      b-navbar-nav
        b-nav-item {{ nomeCidade }}
      b-navbar-nav.ml-auto
        b-nav-item
          img.icon-sub(src="../assets/imgs/icon-house.svg")
          | Home
        b-nav-item
          img.icon-sub(src="../assets/imgs/icon-diversao.svg")
          | Diversão
        b-nav-item
          img.icon-sub(src="../assets/imgs/icon-suaturma.svg")
          | Sua turma
        b-nav-item
          img.icon-sub(src="../assets/imgs/promocao.svg")
          | Promoções
        b-nav-item
          img.icon-sub(src="../assets/imgs/icon-ajuda.svg")
          |Ajuda
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
