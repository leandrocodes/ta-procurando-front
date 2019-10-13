<template lang="pug">
  .appHeader
    header.header
      b-nav(align='left' @click="open = !open").menu
        b-nav-item
          nuxt-link(to='/')
            .header-logo
        b-nav-item.burguer
          .line.line1
          .line.line2
          .line.line3

      b-nav(align='right').nav-links
        div.nav-item
          b-nav-item Anúncie seu Imóvel
            div.left-line
            div.right-line
            div.bottom-line
            div.top-line
        div.nav-item
          b-nav-item Viajante
            div.left-line
            div.right-line
            div.bottom-line
            div.top-line
        div.nav-item
          b-nav-item Anunciante
            div.left-line
            div.right-line
            div.bottom-line
            div.top-line
        div.nav-item
          nuxt-link(to='/contato')
            b-nav-item Contato
              div.left-line
              div.right-line
              div.bottom-line
              div.top-line

      b-nav.nav-mobile(v-if="open" align='right' is-nav-bar='true')
        div.nav-item
          b-nav-item Viajante
            div.left-line
            div.right-line
            div.bottom-line
            div.top-line
        div.nav-item
          b-nav-item Anunciante
            div.left-line
            div.right-line
            div.bottom-line
            div.top-line
        div.nav-item
          b-nav-item Anúnciar
            div.left-line
            div.right-line
            div.bottom-line
            div.top-line
        div.nav-item
          nuxt-link(to='/contato')
            b-nav-item Contato

              div.left-line
              div.right-line
              div.bottom-line
              div.top-line
    AppNavbar
</template>
<script>
import AppNavbar from './AppNavbar'
export default {
  name: 'AppHeader',
  components: {
    AppNavbar
  },
  data () {
    return {
      open: false
    }
  }
}
</script>

<style lang="scss" scoped>
@media screen and (max-width: 425px){
}
</style>
