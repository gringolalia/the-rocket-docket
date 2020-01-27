<template lang="pug">
#app
	nav.uk-navbar-container.uk-margin(uk-navbar uk-sticky)
		.uk-navbar-left.with.dignity
			a.uk-navbar-item.uk-logo.with.dignity(href='/') 
				i.fas.fa-sun.fa-2x.uk-margin-small-right
				| Engenho Novo LLC
		.uk-navbar-right
			.uk-navbar-item
				button.uk-button.uk-button-default.uk-button-large(class="uk-visible@m" type="button")
					i.material-icons.uk-margin-small-right keyboard_arrow_down
					|  Planets
				div(uk-dropdown="mode: click")
					ul.uk-nav.uk-dropdown-nav
						li.uk-nav-header Non-Fictional
						li.uk-active
							a(href='/mercury') Mercury
						li
							a(href='/venusl') Venus
						li
							a(href='/earth') Earth 
						li
							a(href='/mars') Mars
						li
							a(href='/jupiter') Jupiter
						li
							a(href='/saturn') Saturn
						li
							a(href='/uranus') Uranus
						li
							a(href='/neptune') Neptune

						li.uk-nav-divider
						li.uk-nav-header Fictional
						li
							a(href='/vulcan') Vulcan
						li
							a(href='/vogsphere') Vogsphere
						li
							a(href='/krytpon') Krypton
						li
							a(href='/tatooine') Tatooine
						li
							a(href='/solaris') Solaris

				button.uk-button.uk-button-default.uk-button-large.uk-margin-small-left(type="button" uk-toggle='target: #offcanvas-usage' class="uk-visible@m")
					i.material-icons.uk-margin-small-right beach_access
					| Kidding Aside


				#offcanvas-usage.uk-width-large(uk-offcanvas="flip:true")
					.uk-offcanvas-bar( style="width: 400px")
						button.uk-offcanvas-close(type='button' uk-close)
						h3
							i.fas.fa-sun.fa-2x.uk-margin-small-right
							| Engenho Novo LLP
						p.uk-text-left Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
						button.uk-button.uk-button-large.uk-button-danger.uk-margin-large-bottom
							i.material-icons.md-48.uk-margin-small-right directions_run
							| Acknowledge
						ul.uk-iconnav.uk-flex-center
							li
								a(href='#' uk-icon='icon: code; ratio: 2')
							li
								a(href='#' uk-icon='icon: link; ratio: 2')
							li
								a(href='#' uk-icon='icon: social;ratio: 2')
							li
								a(href='#' uk-icon='icon: git-fork; ratio: 2')
							li
								a(href='#' uk-icon='icon: quote-right; ratio: 2')

	//- router-view
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
	name: 'app',
	components: {
		HelloWorld
	}
}
</script>

<style lang="less">
#app, body {
	font-family: 'News Cycle', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
}
</style>
