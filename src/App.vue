<template>
	<div class="app-container">
		<TheSidebar />
		<TheCollectionCardContainer />
	</div>
	<!-- <img alt="Vue logo" src="./assets/logo.png" /> -->

	<!-- <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
</template>

<script lang="ts">
	import { Options, Vue } from "vue-class-component";
	import HelloWorld from "./components/HelloWorld.vue";
	import TheSidebar from "./components/Sidebar/TheSidebar.vue";
	import TheCollectionCardContainer from "./components/CollectionCard/TheCollectionCardContainer.vue";

	@Options({
		components: {
			HelloWorld,
			TheSidebar,
			TheCollectionCardContainer,
		},
	})
	export default class App extends Vue {}
</script>

<style lang="scss">
	#app {
		font-family: "Gilroy", Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		background-color: #414354;
	}
	body {
		margin: 0;
	}
	.app-container {
		display: grid;
		grid-template-columns: 300px 1fr;
	}
</style>
