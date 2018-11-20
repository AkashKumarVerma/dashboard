<template>
	<div class="home--wrapper pl-10-sm-and-up">
		<v-container align-content-start fluid fill-height>
			<v-layout align-start justify-center wrap>
				<v-card hover height="270px" width="270px" min-width="270px" class="pa-3 ma-3" v-for="project in projects">
					<img :src="project.logo" alt="">
					<h3>{{project.title}}</h3>
					<a><v-icon small>link</v-icon> {{project.link}}</a>
					<p class="description mt-3">{{project.description}}</p>
					<v-flex d-flex>
				    <v-layout row wrap class="details-wrapper">
				    	<div class="progress-bar">
								<v-progress-linear
						      color="#42b993"
						      background-color="#e2e2e2"
						      height="3"
						      :value="project.progress"
						    ></v-progress-linear>
				    	</div>
				    	<div class="details">
								<v-chip label small d-block color="#ffe9ea" text-color="#ec7272" class="pl-0">
									<v-icon color="#ec7272" left small>access_time</v-icon>&nbsp; {{project.time}} days left
								</v-chip>
								<v-avatar tile size="20" class="ma-1" v-for="user in project.users">
									<img :src="user" alt="">
								</v-avatar>
				    	</div>
				    </v-layout>
					</v-flex>
				</v-card>
			</v-layout>
		</v-container>
	</div>
</template>

<script>
export default {
  name: 'Home',
  data () {
  	return {
  		projects: [
  			{
  				title: 'Sports Interactive',
  				link: 'sportsinteractive.com',
  				logo: require('@/assets/logo-1.png'),
  				description: 'Web resource which contains all abouttransfer in the world of sports',
  				progress: '94',
  				time: '2',
  				users: [
  					require('@/assets/user-1.png'),
  					require('@/assets/user-2.png')
  				]
  			},
  			{
  				title: 'Homechoice',
  				link: 'homechoice.com',
  				logo: require('@/assets/logo-2.png'),
  				description: 'Resource that allows you to buy a cheap accomodation in a steep price',
  				progress: '54',
  				time: '4',
  				users: [
  					require('@/assets/user-3.png'),
  					require('@/assets/user-4.png'),
  					require('@/assets/user-5.png')
  				]
  			},
  			{
  				title: 'Big Money Real Estate',
  				link: 'bigmoneyrealestate.com',
  				logo: require('@/assets/logo-3.png'),
  				description: 'Agency that specializes in luxuary real estate in Monte Carlo',
  				progress: '59',
  				time: '5',
  				users: [
  					require('@/assets/user-4.png'),
  					require('@/assets/user-5.png'),
  					require('@/assets/user-6.png')
  				]
  			},
  			{
  				title: 'Springfield Media',
  				link: 'springfieldmedia.com',
  				logo: require('@/assets/logo-4.png'),
  				description: 'Multimedia content studio. Simply unique',
  				progress: '48',
  				time: '7',
  				users: [
  					require('@/assets/user-8.png'),
  					require('@/assets/user-2.png')
  				]
  			},
  			{
  				title: 'Regular Logistics',
  				link: 'regularlogistics.com',
  				logo: require('@/assets/logo-5.png'),
  				description: 'Logistic company that specializes in regular shipments within europe',
  				progress: '46',
  				time: '9',
  				users: [
  					require('@/assets/user-2.png'),
  					require('@/assets/user-7.png'),
  					require('@/assets/user-4.png')
  				]
  			},
  			{
  				title: 'Foursquare agency',
  				link: 'foursquareagency.com',
  				logo: require('@/assets/logo-6.png'),
  				description: 'Creative agency that deals with advertising and marketing',
  				progress: '39',
  				time: '11',
  				users: [
  					require('@/assets/user-8.png'),
  					require('@/assets/user-3.png'),
  					require('@/assets/user-5.png'),
  					require('@/assets/user-7.png')
  				]
  			},
  			{
  				title: 'Piece Studio',
  				link: 'piecestudio.com',
  				logo: require('@/assets/logo-7.png'),
  				description: 'Studio that specializes in interactive events',
  				progress: '34',
  				time: '12',
  				users: [
  					require('@/assets/user-8.png'),
  					require('@/assets/user-5.png')
  				]
  			},
  			{
  				title: 'Legacy Foundation',
  				link: 'legacyfoundation.com',
  				logo: require('@/assets/logo-1.png'),
  				description: 'Foundation that helps people to be more confident and achive their goals',
  				progress: '32',
  				time: '12',
  				users: [
  					require('@/assets/user-3.png'),
  					require('@/assets/user-4.png'),
  					require('@/assets/user-2.png')
  				]
  			}
  		]
  	}
  }
}
</script>

<style lang="sass" scoped>
.home--wrapper
	width: 100vw
	// padding-left: 50px
	background-color: #fafafa
	.v-card
		border-radius: 10px

	.v-card__title
		width: 40px
		height: 40px
		border-radius: 10px !important
		background-color: #f9d12b
		font-size: 35px
		font-weight: 800
		font-style: italic
		line-height: 40px
		color: #414141
	h3
		margin-top: 10px
		margin-bottom: -5px
	a
		color: #a0a0a0
		font-size: 12px
		font-weight: 300
		i
			margin-right: 3px

	p
		color: #707070
		font-size: 13px
		line-height: 15px
	.details-wrapper
		position: absolute
		width: 88%
		bottom: 15px
	.progress-bar
		width: 100%
		height: auto
	.details
		width: 100%
		height: auto
		.v-chip.v-chip--small
			width: 80px
			span.v-chip__content
				padding: 0
			font-size: 10px
			i.v-icon
				font-size: 8px
				margin-right: 0
		.v-avatar.v-avatar--tile
			float: right
</style>
