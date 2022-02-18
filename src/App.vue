<template>
	<v-card>
		<!-- <v-system-bar></v-system-bar> -->
		<AppBar></AppBar>
		<NavigationDrawers></NavigationDrawers>
		<v-main>
			<v-container fluid>
				<router-view></router-view>
			</v-container>
		</v-main>
		<v-footer app></v-footer>
		<!-- <v-footer-navigation></v-footer-navigation> -->
	</v-card>
</template>

<script>
import NavigationDrawers from "./views/layout/NavigationDrawers.vue";
import AppBar from "./views/layout/AppBar.vue";
export default {
	name: "App",
	data() {
		return {};
	},
	components: { NavigationDrawers, AppBar },
};
</script>
