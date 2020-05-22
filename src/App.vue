<template>
	<div id="app w-screen h-screen ">
		<QRCodeConfiguration class="relative float-left w-8/12 h-screen" />
		<QRCodeViewerComponent class="relative float-left w-4/12 h-screen border-r" />
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
