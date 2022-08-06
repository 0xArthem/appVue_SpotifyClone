<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <MiddleContent></MiddleContent>
  <SideBarMenu></SideBarMenu>
  <BottomBarCommande></BottomBarCommande>
</template>

<script>
import SideBarMenu from './components/side-bar-menu.vue'
import BottomBarCommande from './components/bottom-bar-commande.vue'
import MiddleContent from './components/middle-content.vue'

export default {
  name: 'App',
  components: {
    SideBarMenu,
    BottomBarCommande,
    MiddleContent
}
}
</script>

<style>
body{
  overflow-y: hidden;
  overflow-x: hidden;
}
#app {
  font-family: 'Signika Negative', sans-serif;
}
</style>
