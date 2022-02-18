<template>
	<v-navigation-drawer
		v-model="drawer"
		:mini-variant.sync="mini"
		dark
		src="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
		permanent
		app
	>
		<v-list>
			<v-list-item @click.stop="mini = !mini" link>
				<v-list-item-icon>
					<v-icon>mdi-menu</v-icon>
				</v-list-item-icon>
				<v-list-item-content>
					<v-list-item-title>{{
						$t("title.menu")
					}}</v-list-item-title>
				</v-list-item-content>
			</v-list-item>
			<v-list-item v-for="item in items" :key="item.title" link>
				<v-list-item-icon>
					<v-icon>{{ item.icon }}</v-icon>
				</v-list-item-icon>
				<v-list-item-content>
					<v-list-item-title>{{ item.title }}</v-list-item-title>
				</v-list-item-content>
			</v-list-item>
		</v-list>
	</v-navigation-drawer>
</template>

<script>
export default {
	data() {
		return {
			drawer: false,
			items: [
				{ title: "Home", icon: "mdi-home" },
				{ title: "My Account", icon: "mdi-account" },
				{ title: "Users", icon: "mdi-account-group-outline" },
			],
			mini: true,
		};
	},
};
</script>

<style></style>
