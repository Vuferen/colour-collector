<template>
	<div class="sidebar">
		<span class="sidebar-title">Collections</span>
		<SidebarFolder></SidebarFolder>
		<SidebarFolder></SidebarFolder>
	</div>
</template>

<script lang="ts">
	import { Options, Vue } from "vue-class-component";
	import SidebarFolder from "./SidebarFolder.vue";

	@Options({
		components: {
			SidebarFolder,
		},
	})
	export default class TheSidebar extends Vue {}
</script>

<style lang="scss">
	.sidebar {
		width: 100%;
		height: 100vh;
		background-color: #1a1c24;
		display: flex;
		flex-direction: column;
		padding: 25px 20px;
		box-sizing: border-box;
		&-title {
			color: rgb(233, 241, 241);
			// text-align: left;
			font-size: 28px;
			font-family: "Gilroy";
			letter-spacing: 1px;
			margin-bottom: 10px;
		}
	}
</style>
