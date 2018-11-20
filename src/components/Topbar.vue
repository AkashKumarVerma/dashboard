<template>
	    <v-toolbar app clipphed-left fixed flat height="80px" class="elevation-1 pl-5" color="#fff" >
      <v-layout row justify-space-between>
        <v-flex sm2>
          <h1>Projects</h1>
        </v-flex>
        <v-flex sm3>
          <v-layout row justify-center align-center class="menu">
            <span class="ma-2">All</span>
            <span class="ma-2">Current</span>
            <span class="ma-2">Pending</span>
            <span class="ma-2">Completed</span>
            <span class="ma-2">Failed</span>
          </v-layout>
        </v-flex>
        <v-flex sm2>
          <v-icon>search</v-icon>
          <v-badge color="red" class="ml-4">
            <span slot="badge" style="font-size: 10px;">2</span>
            <v-icon>notification_important</v-icon>
          </v-badge>

           <v-menu
            transition="slide-y-transition"
            bottom
            >
              <v-avatar slot="activator" size="35" class="ml-5">
                <img src="https://cdn.vuetifyjs.com/images/lists/1.jpg" alt="">
              </v-avatar>
              <v-list>
                <v-list-tile>
                  <v-list-tile-title>Item 1</v-list-tile-title>
                </v-list-tile>
                <v-list-tile>
                  <v-list-tile-title>Item 1</v-list-tile-title>
                </v-list-tile>
                <v-list-tile>
                  <v-list-tile-title>Item 1</v-list-tile-title>
                </v-list-tile>
                <v-list-tile>
                  <v-list-tile-title>Item 1</v-list-tile-title>
                </v-list-tile>

              </v-list>
            </v-menu>
        </v-flex>
      </v-layout>
    </v-toolbar>
</template>

<script>
export default {
	name: 'Topbar'
}
</script>

<style lang="sass" scoped>

</style>