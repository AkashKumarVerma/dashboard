<template>
  <v-app>
    <!-- <v-navigation-drawer  app></v-navigation-drawer> -->
    <topbar/>
    <sidebar/>
    <v-content>
      <router-view />
    </v-content>
    <!-- <v-footer app></v-footer> -->
  </v-app>
</template>

<script>
import Sidebar from './components/Sidebar'
import Topbar from './components/Topbar'

export default {
  name: 'App',
  components: {
    Sidebar,
    Topbar
  },
  data () {
    return {
      //
    }
  }
}
</script>

<style lang="sass" scoped>
.v-content__wrap
  background-color: #f8f9fb

  .menu
    span
      margin: 0 10px
</style>