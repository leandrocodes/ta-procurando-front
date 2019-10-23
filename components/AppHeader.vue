<template lang="pug">
  .appHeader
    header.header
      b-nav(align='left').menu
        .row
          b-nav-item
            nuxt-link(to='/home')
              .header-logo

          b-nav-item.burguer(@click="burgerAction" :class="{'active': burguerClassActive}")
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

      transition(name="slide")
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
      open: false,
      burguerClassActive: false
    }
  },
  methods: {
    burgerAction () {
      this.open = !this.open
      this.burguerClassActive = !this.burguerClassActive
    }
  }
}
</script>

<style lang="scss" scoped>

.slide-enter-active,
.slide-leave-active {
  transition: all 0.2s;
  max-height: 100px;
}

.slide-enter, .slide-leave-to /* .fade-leave-active em versões anteriores a 2.1.8 */ {
  opacity: 0;
  max-height: 0px;
}

.active{
  .line2{
    opacity: 0;
  }
  .line1{
    transform: rotate(-45deg);
    top: 14px;
  }
  .line3{
    transform: rotate(45deg);
  }
}

</style>
