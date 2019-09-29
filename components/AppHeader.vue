<template>
  <header class="header">
    <b-nav align="left">
      <b-nav-item>
        <nuxt-link to="/">
          <img class="header-logo" src="../assets/imgs/logomarca-taprocurando.svg">
        </nuxt-link>
      </b-nav-item>
    </b-nav>
    <b-nav align="right">
      <b-nav-item>Anúncie seu Imóvel</b-nav-item>
      <b-nav-item>Viajante</b-nav-item>
      <b-nav-item>Anunciante</b-nav-item>
      <b-nav-item>Contato</b-nav-item>
    </b-nav>
  </header>
</template>
<script>
export default {
  name: 'AppHeader'
}
</script>

<style lang="scss" scoped>
</style>
