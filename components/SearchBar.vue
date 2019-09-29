<template lang="pug">
  header.header
    b-nav(align='left')

      b-nav-item
        nuxt-link(to='/')
          img.header-logo(src='../assets/imgs/logomarca-taprocurando.svg')

    b-nav(align='right')
      div.nav-item
        b-nav-item Anúncie seu Imóvel
        animation-group
          div.left-line
          div.right-line
          div.bottom-line
          div.top-line

      div.nav-item
        b-nav-item Viajante
        animation-group
          div.left-line
          div.right-line
          div.bottom-line
          div.top-line

      div.nav-item
        b-nav-item Anunciante
        animation-group
          div.left-line
          div.right-line
          div.bottom-line
          div.top-line

      div.nav-item
        nuxt-link(to='/contato')
          b-nav-item Contato
          animation-group
            div.left-line
            div.right-line
            div.bottom-line
            div.top-line
</template>
<script>
export default {
  name: 'AppHeader'
}
</script>

<style lang="scss" scoped>
</style>
