<template lang="pug">
  .index
    AppHeader
    section.busca
      .tabs
        .tab.casa
          img(src="../assets/imgs/icon-casa.svg")
          |Casa
        .tab.pousada Pousada
        .tab.hotel Hotel
        .tab.beira-mar Beira-mar
        .tab.sitio Sitio
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
