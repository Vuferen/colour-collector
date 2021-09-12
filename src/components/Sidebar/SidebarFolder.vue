<template>
	<details class="sidebar--folder">
		<summary class="sidebar--folder-header-title" @click.right="menu()">
			<input type="text" name="" :value="title" />
		</summary>
		<div class="sidebar--folder-content">
			<SidebarCollection></SidebarCollection>
			<SidebarCollection></SidebarCollection>
		</div>
	</details>
</template>

<script lang="ts">
	import { Options, Vue } from "vue-class-component";
	import SidebarCollection from "./SidebarCollection.vue";

	@Options({
		components: {
			SidebarCollection,
		},
		data() {
			return {
				title: "Awesome colours",
			};
		},
		methods: {
			menu() {},
			rename() {},
			delete() {},
		},
	})
	export default class SidebarFolder extends Vue {}
</script>

<style lang="scss">
	.sidebar--folder {
		color: rgb(196, 204, 207);
		margin-bottom: 5px;
		font-size: 16px;
		&-header-title {
			border-radius: 15px;
			padding: 5px 13px;
			cursor: pointer;
			&:hover {
				background-color: #262933;
			}
			input {
				pointer-events: none;
				background: transparent;
				color: inherit;
				font-family: inherit;
				font-size: inherit;
				border: none;
			}
		}
		&-content {
			// margin-top: 5px;
			margin-left: 17px;
			display: flex;
			flex-direction: column;
		}
	}
</style>
