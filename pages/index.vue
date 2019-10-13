<template lang="pug">
  .index
    AppHeader
    section.busca
      div.tabs
        div.tab.casa(@click="toggleTab('casa')" :class="{active: casa.isActive}")
          img(src="../assets/imgs/icon-casa.svg")
          | Casa
        div.tab.pousada(@click="toggleTab('pousada')" :class="{active: pousada.isActive}")
          img(src="../assets/imgs/icon-pousada.svg")
          | Pousada
        div.tab.hotel(@click="toggleTab('hotel')" :class="{active: hotel.isActive}")
          img(src="../assets/imgs/icon-hotel.svg")
          | Hotel
        div.tab.beira-mar(@click="toggleTab('beiramar')" :class="{active: beiramar.isActive}")
          img(src="../assets/imgs/icon-beiramar.svg")
          | Beira-mar
        div.tab.sitio(@click="toggleTab('sitio')" :class="{active: sitio.isActive}")
          img(src="../assets/imgs/icon-sitio.svg")
          | Sítio
      div.search-box
        div.search-casa(v-show="casa.isActive")
          form.form-search
            .destino
              label(for="destino") Digite seu destino:
              .input
                img(src="../assets/imgs/home-localizacao.svg")
                input(type="text" placeholder="ex: Belo Horizonte" style="width: 250px")
            .datas
              label(for="data") Datas:
              .input
                input(type="text" placeholder="Ida")
                input(type="text" placeholder="Volta")
            .hospedes(@click="openDropdown")
              label(for="hospedes") Hóspedes:
                .dropdown
                  p(v-if="!hospedes") Selecione os hóspedes
                  font-awesome-icon(:icon="['fas', 'angle-down']")
                .menu(v-if="openDropdownMenu")
                  | teste123
            .buscar
              a.btn Buscar
                font-awesome-icon(:icon="['fas', 'angle-right']")
        div.search-casa(v-show="pousada.isActive")
          | Pousada
        div.search-casa(v-show="hotel.isActive")
          | Hotel
        div.search-casa(v-show="beiramar.isActive")
          | Beira-mar
        div.search-casa(v-show="sitio.isActive")
          | Sítio
</template>

<script>
import AppHeader from '../components/AppHeader'
export default {
  components: {
    AppHeader
  },
  data () {
    return {
      casa: {
        isActive: true
      },
      pousada: {
        isActive: false
      },
      hotel: {
        isActive: false
      },
      beiramar: {
        isActive: false
      },
      sitio: {
        isActive: false
      },
      hospedes: null,
      openDropdownMenu: false
    }
  },
  methods: {
    toggleTab (tab) {
      switch (tab) {
        case 'casa':
          this.casa.isActive = !this.casa.isActive
          this.pousada.isActive = false
          this.hotel.isActive = false
          this.beiramar.isActive = false
          this.sitio.isActive = false
          break

        case 'pousada':
          this.casa.isActive = false
          this.pousada.isActive = !this.pousada.isActive
          this.hotel.isActive = false
          this.beiramar.isActive = false
          this.sitio.isActive = false
          break

        case 'hotel':
          this.casa.isActive = false
          this.pousada.isActive = false
          this.hotel.isActive = !this.hotel.isActive
          this.beiramar.isActive = false
          this.sitio.isActive = false
          break

        case 'beiramar':
          this.casa.isActive = false
          this.pousada.isActive = false
          this.hotel.isActive = false
          this.beiramar.isActive = !this.beiramar.isActive
          this.sitio.isActive = false
          break

        case 'sitio':
          this.casa.isActive = false
          this.pousada.isActive = false
          this.hotel.isActive = false
          this.beiramar.isActive = false
          this.sitio.isActive = !this.sitio.isActive
          break
      }
    },
    openDropdown () {
      this.openDropdownMenu = !this.openDropdownMenu
    }
  }
}
</script>

<style>
</style>
