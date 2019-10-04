<template lang="pug">
  div.appNavbar
    b-navbar(variant="primary" type="dark").navApp
      b-navbar-nav.ml-auto.mr-auto
        b-nav-item.nome-cidade.mr-0
          font-awesome-icon(:icon="['fas', 'map-marker-alt']")
          | {{ nomeCidade }}
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
        b-nav-item.notification-btn Notificação

    b-navbar(variant="primary" type="dark" v-show="open").mobile-nav
      b-navbar-nav.ml-auto.mr-auto()
        b-nav-item.nome-cidade.mr-0
          font-awesome-icon(:icon="['fas', 'map-marker-alt']")
          | {{ nomeCidade }}
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
        b-nav-item.notification-btn Notificação
</template>
<script>
export default {
  name: 'AppHeader',
  data () {
    return {
      nomeCidade: 'Belo Horizonte - MG',
      open: false
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
