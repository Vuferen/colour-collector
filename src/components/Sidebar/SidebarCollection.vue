<template>
	<div class="sidebar--collection">
		<span class="sidebar--collection-title">A coolerful collection</span>
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
	export default class SidebarCollection extends Vue {}
</script>

<style lang="scss">
	.sidebar--collection {
		// margin-top: 5px;
		// margin-left: 15px;
		padding: 5px 13px;
		border-radius: 15px;
		width: fit-content;
		cursor: pointer;
		&:hover {
			background-color: #262933;
		}
	}
</style>
