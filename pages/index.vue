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
            .hospedes
              label(for="hospedes") Hóspedes:
                .dropdown(@click="openDropdown")
                  p(v-if="!hospedes") Selecione os hóspedes
                  p(v-else) {{nAdultos}} Adultos e {{nCriancas}} Crianças
                  font-awesome-icon(:icon="['fas', 'angle-down']")
                transition(name="showIn")
                  .menu(v-if="openDropdownMenu")
                    .adultos
                      | {{ nAdultos }} Adultos
                      a.btn(@click='nAdultos--') -
                      a.btn(@click='nAdultos++') +
                    hr
                    .criancas
                      | {{ nCriancas }} Crianças
                      a.btn(@click='nCriancas--') -
                      a.btn(@click='nCriancas++') +
            .buscar
              a.btn Buscar
                font-awesome-icon(:icon="['fas', 'angle-right']")

        div.search-casa(v-show="pousada.isActive")
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
            .hospedes
              label(for="hospedes") Hóspedes:
                .dropdown(@click="openDropdown")
                  p(v-if="!hospedes") Selecione os hóspedes
                  p(v-else) {{nAdultos}} Adultos e {{nCriancas}} Crianças
                  font-awesome-icon(:icon="['fas', 'angle-down']")
                transition(name="showIn")
                  .menu(v-if="openDropdownMenu")
                    .adultos
                      | {{ nAdultos }} Adultos
                      a.btn(@click='nAdultos--') -
                      a.btn(@click='nAdultos++') +
                    hr
                    .criancas
                      | {{ nCriancas }} Crianças
                      a.btn(@click='nCriancas--') -
                      a.btn(@click='nCriancas++') +
            .buscar
              a.btn Buscar
                font-awesome-icon(:icon="['fas', 'angle-right']")

        div.search-casa(v-show="hotel.isActive")
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
            .hospedes
              label(for="hospedes") Hóspedes:
                .dropdown(@click="openDropdown")
                  p(v-if="!hospedes") Selecione os hóspedes
                  p(v-else) {{nAdultos}} Adultos e {{nCriancas}} Crianças
                  font-awesome-icon(:icon="['fas', 'angle-down']")
                transition(name="showIn")
                  .menu(v-if="openDropdownMenu")
                    .adultos
                      | {{ nAdultos }} Adultos
                      a.btn(@click='nAdultos--') -
                      a.btn(@click='nAdultos++') +
                    hr
                    .criancas
                      | {{ nCriancas }} Crianças
                      a.btn(@click='nCriancas--') -
                      a.btn(@click='nCriancas++') +
            .buscar
              a.btn Buscar
                font-awesome-icon(:icon="['fas', 'angle-right']")

        div.search-casa(v-show="beiramar.isActive")
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
            .hospedes
              label(for="hospedes") Hóspedes:
                .dropdown(@click="openDropdown")
                  p(v-if="!hospedes") Selecione os hóspedes
                  p(v-else) {{nAdultos}} Adultos e {{nCriancas}} Crianças
                  font-awesome-icon(:icon="['fas', 'angle-down']")
                transition(name="showIn")
                  .menu(v-if="openDropdownMenu")
                    .adultos
                      | {{ nAdultos }} Adultos
                      a.btn(@click='nAdultos--') -
                      a.btn(@click='nAdultos++') +
                    hr
                    .criancas
                      | {{ nCriancas }} Crianças
                      a.btn(@click='nCriancas--') -
                      a.btn(@click='nCriancas++') +
            .buscar
              a.btn Buscar
                font-awesome-icon(:icon="['fas', 'angle-right']")

        div.search-casa(v-show="sitio.isActive")
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
            .hospedes
              label(for="hospedes") Hóspedes:
                .dropdown(@click="openDropdown")
                  p(v-if="!hospedes") Selecione os hóspedes
                  p(v-else) {{nAdultos}} Adultos e {{nCriancas}} Crianças
                  font-awesome-icon(:icon="['fas', 'angle-down']")
                transition(name="showIn")
                  .menu(v-if="openDropdownMenu")
                    .adultos
                      | {{ nAdultos }} Adultos
                      a.btn(@click='nAdultos--') -
                      a.btn(@click='nAdultos++') +
                    hr
                    .criancas
                      | {{ nCriancas }} Crianças
                      a.btn(@click='nCriancas--') -
                      a.btn(@click='nCriancas++') +
            .buscar
              a.btn Buscar
                font-awesome-icon(:icon="['fas', 'angle-right']")
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
      openDropdownMenu: false,
      nAdultos: 5,
      nCriancas: 2
    }
  },
  watch: {
    nAdultos () {
      this.hospedes = true
      return this.hospedes
    },
    nCriancas () {
      this.hospedes = true
      return this.hospedes
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
.showIn-enter-active, .showIn-leave-active {
  transition: all .2s;
  max-height: 100px;
}
.showIn-enter, .showIn-leave-to /* .fade-leave-active em versões anteriores a 2.1.8 */ {
  opacity: 0;
  max-height: 0px;
}
</style>
