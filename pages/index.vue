<template lang="pug">
  .index
    AppHeader
    section.busca
      div.tabs
        div.tab.casa
          img(src="../assets/imgs/icon-casa.svg")
          | Casa
        div.tab.pousada
          img(src="../assets/imgs/icon-pousada.svg")
          | Pousada
        div.tab.hotel
          img(src="../assets/imgs/icon-hotel.svg")
          | Hotel
        div.tab.beira-mar
          img(src="../assets/imgs/icon-beiramar.svg")
          | Beira-mar
        div.tab.sitio
          img(src="../assets/imgs/icon-sitio.svg")
          |Sitio
</template>

<script>
import AppHeader from '../components/AppHeader'
export default {
  components: {
    AppHeader
  }
}
</script>

<style>
</style>
