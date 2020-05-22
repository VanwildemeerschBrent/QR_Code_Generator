<template>
	<div class="flex w-screen h-screen app bg-appBlueLight">
		<QRCodeConfiguration class="w-7/12 h-screen qr-configuration-container" />
		<QRCodeViewerComponent class="w-5/12 text-white qr-viewer-container bg" />
	</div>
</template>

<script lang="ts">
	import { Component, Vue } from "vue-property-decorator";
	import QRCodeViewerComponent from "./components/QRCodeViewer/QRCodeViewerComponent.vue";
	import QRCodeConfiguration from "./components/QRCodeConfigurator/QRCodeConfigurationComponent.vue";

	@Component({
		components: {
			QRCodeViewerComponent,
			QRCodeConfiguration
		}
	})
	export default class App extends Vue {}
</script>

<style lang="scss" scoped>
	.app {
		display: flex;
		flex-direction: row;
	}
</style>
