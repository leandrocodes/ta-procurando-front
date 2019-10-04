<template lang="pug">
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

    b-nav.nav-mobile(v-if="open")
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
        b-nav-item Anúnciar
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
  name: 'AppHeader',
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
