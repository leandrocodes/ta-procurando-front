<template lang="pug">
  div.appNavbar
    b-navbar(variant="primary" type="dark").navApp

      b-navbar-nav.mr-5
        b-nav-item.nome-cidade.mr-5
          font-awesome-icon(:icon="['fas', 'map-marker-alt']")
          | {{ nomeCidade }}

      b-navbar-nav.mr-auto.ml-auto
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
