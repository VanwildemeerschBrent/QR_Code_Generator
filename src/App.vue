<template>
	<div id="app w-screen h-screen ">
		<QRCodeViewerComponent class="h-screen w-8/12 relative float-left border-r" />
		<QRCodeConfiguration class="h-screen w-4/12 relative float-left" />
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

<style lang="scss">
</style>
