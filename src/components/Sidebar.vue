<template>
	<v-navigation-drawer
    :mini-variant="mini"
    v-model="drawer"
    disable-resize-watcher
    fixed
    height="100vh"
    mini-variant-width="50"
    hide-overlay
    stateless
    class="aside hidden-sm-and-down">
    <div class="logo-wrapper pt-3">
			<img class="user-image" src="@/assets/logo.svg">
    </div>

    <div class="menu--wrapper">
			<v-layout justify-center align-center fill-height>
		    <v-list>
		    	<v-list-tile>
		    		<v-icon color="#ffffff">home</v-icon>
		    	</v-list-tile>
		    	<v-list-tile>
		    		<v-icon color="#ffffff"
		    			@click="$router.push('/')"
		    			:class="{selected : $route.path == '/'}">dashboard</v-icon>
		    	</v-list-tile>
		    	<v-list-tile>
		    		<v-icon color="#ffffff">calendar_today</v-icon>
		    	</v-list-tile>
		    	<v-list-tile>
		    		<v-icon
		    			color="#ffffff"
		    			light
		    			@click="$router.push('/messages')"
		    			:class="{selected : $route.path == '/messages'}">chat</v-icon>
		    	</v-list-tile>
		    	<v-list-tile>
		    		<v-icon color="#ffffff">access_time</v-icon>
		    	</v-list-tile>
		    	<v-list-tile>
		    		<v-icon color="#ffffff">perm_identity</v-icon>
		    	</v-list-tile>
		    	<v-list-tile>
		    		<v-icon color="#ffffff">settings</v-icon>
		    	</v-list-tile>
		    </v-list>
	   	</v-layout>
    </div>

  </v-navigation-drawer>
</template>

<script>
export default {
  name: 'Sidebar',
  data () {
    return {
      drawer: true,
      items: [
        { title: 'Home', icon: 'dashboard' },
        { title: 'About', icon: 'question_answer' }
      ],
      mini: true,
      right: null
    }
  },
  mounted () {
  	console.log(this.$route.path)
  }
}
</script>

<style lang="sass" scoped>
.v-navigation-drawer--mini-variant.theme--light
	background: #0074E8

	.logo-wrapper
		width: 100%
		height: auto
		display: flex
		justify-content: center
		.user-image
			display: inline-block
			width: 30px
			height: 30px

	.menu--wrapper
		height: calc(100vh - 100px)

		.v-icon.theme--light
			width: 40px
			height: 40px
			cursor: pointer
			border-radius: 10px
			&:hover
				background: darken(#0074e8, 10)

			&.selected
				background: darken(#0074e8, 15)

</style>
