<template lang="pug">
  header.header
    b-nav(align='left')
      b-nav-item
        nuxt-link(to='/')
          img.header-logo(src='../assets/imgs/logomarca-taprocurando.svg')
    b-nav(align='right')
      div.nav-item
        b-nav-item Anúncie seu Imóvel
        div.left-line
        div.right-line
        div.bottom-line
        div.top-line
      b-nav-item Viajante
      b-nav-item Anunciante
      b-nav-item Contato
</template>
<script>
export default {
  name: 'AppHeader'
}
</script>

<style lang="scss" scoped>
</style>
