<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <SideBarMenu></SideBarMenu>
  <BottomBarCommande></BottomBarCommande>
</template>

<script>
import SideBarMenu from './components/side-bar-menu.vue'
import BottomBarCommande from './components/bottom-bar-commande.vue'

export default {
  name: 'App',
  components: {
    SideBarMenu,
    BottomBarCommande
}
}
</script>

<style>
#app {
  font-family: 'Signika Negative', sans-serif;
}
</style>
