<template>
  <section class="container" style="position: absolute; background-color: rgba(0,0,0,0.95);">
    <div class="nav-container d-flex justify-content-between align-items-center p-4" >
      <router-link class="logo" to="/">
        <img :src="usedlogo" alt="tic&tac logo" style="width:100px">
      </router-link>
      
      <div v-if="isMobile" class="burger-menu d-flex justify-content-center align-items-center">
        <img v-if="isNavbarMobileOpen" :src="cross" alt="croix de fermeture du burger menu" @click="isNavbarMobileOpen = !isNavbarMobileOpen">
        <img v-else :src="burgerMenu" alt="burger menu" @click="isNavbarMobileOpen = !isNavbarMobileOpen">
      </div>
    </div>


    <div v-if="isMobile" class="d-flex flex-column justify-content-center align-items-center" :class="isNavbarMobileOpen ? 'nav-mobile-on p-4' : 'nav-mobile-off'">
      <transition>
        <div v-if="isNavbarMobileOpen">
          <router-link v-if="isNavbarMobileOpen" to="/" class="link mb-3" >Accueil</router-link>
          <router-link v-if="isNavbarMobileOpen" to="/carte.pdf" target="_blank" class="link mb-3">Notre carte</router-link>
          <router-link v-if="isNavbarMobileOpen" to="/contact" class="link mb-3">Réservations</router-link>
          <router-link v-if="isNavbarMobileOpen" to="/about" class="link mb-3">Nous découvrir</router-link>
        </div>
        
      </transition>
    </div>
  </section>
</template>

<script>
import windowWidthMixin from '@/mixins/windowWidthMixin'

export default {
  name:'navbarMobile',
  mixins: [ windowWidthMixin ],
  data() {
    return {
      show: false,
      show: false,
      whitelogo: require('@/assets/img/logo-navbar-white.png'),
      usedlogo : require('@/assets/img/logo-navbar.png'),
      blacklogo: require('@/assets/img/logo-navbar.png'),
      burgerMenu: require('@/assets/icons/burgerMenu.svg'),
      cross: require('@/assets/icons/cross.svg'),
      isNavbarMobileOpen: false,
    }
  },
  methods: {
    toggleNavbar() {
      this.show = !this.show
    }
  },
  setup(){
      
    }
}
</script>

<style lang="scss" scoped>
@font-face {
    font-family: "Noto Sans";
    src: local("Noto Sans"),
    url(@/assets/fonts/NotoSans-Regular.ttf) format("truetype");
}
.link {
  color: white;
  text-decoration: none;
  width: fit-content;
  white-space: nowrap;
  border-radius: 8px;
  padding: 8px 16px;
  transition: 1s;
  display: block;
  text-align: center;
  font-size: 1.25rem;
}
@media screen and (max-width: 768px){
  .link {
    margin-right: 0;
    width: 200px;
  }
}

.v-enter-active, .v-leave-active {
  transition: opacity 2s;
}

.v-enter-from, .v-leave-to {
  opacity: 0;
  transition: 0.25s;
}
.nav-mobile-off{
  height: 0;
  transition: 1s;
}
.nav-mobile-on{
  height: 300px;
  transition: 0.8s;
}
</style>


