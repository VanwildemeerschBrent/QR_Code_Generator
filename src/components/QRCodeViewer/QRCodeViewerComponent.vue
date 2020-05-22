<template>
	<div class="qr-code-viewer-component">
		<div class="ml-8 mr-8 rounded-lg qr-code-viewer-component__content bg-appBlueDark">
			<p>QR Code viewer component</p>
			<img src="../../assets/qr.png" class="w-6/12 ml-auto mr-auto" />
			<div class="mt-4 text-center content_subActions">
				<button
					class="w-8/12 px-4 py-2 mt-4 ml-auto mr-auto font-bold text-white bg-blue-500 rounded rounded-md hover:bg-blue-700"
				>Frame</button>
				<button
					class="w-8/12 px-4 py-2 mt-4 ml-auto mr-auto font-bold text-white bg-blue-500 rounded rounded-md hover:bg-blue-700"
				>Shape & Color</button>
				<button
					class="w-8/12 px-4 py-2 mt-4 ml-auto mr-auto font-bold text-white bg-blue-500 rounded rounded-md hover:bg-blue-700"
				>Logo</button>
			</div>
			<div class="mt-4 text-center content-downloadActions">
				<button
					class="inline-flex items-center px-4 py-2 font-bold text-gray-800 bg-gray-300 rounded hover:bg-gray-400"
				>
					<svg class="w-4 h-4 mr-2 fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
						<path d="M13 8V2H7v6H2l8 8 8-8h-5zM0 18h20v2H0v-2z" />
					</svg>
					<span>JPG</span>
				</button>
				<button
					class="inline-flex items-center px-4 py-2 font-bold text-gray-800 bg-gray-300 rounded hover:bg-gray-400"
				>
					<svg class="w-4 h-4 mr-2 fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
						<path d="M13 8V2H7v6H2l8 8 8-8h-5zM0 18h20v2H0v-2z" />
					</svg>
					<span>SVG</span>
				</button>
			</div>
		</div>
	</div>
</template>

<script lang="ts">
	import { Component, Prop, Vue } from "vue-property-decorator";

	@Component
	export default class QRCodeViewerComponent extends Vue {
		@Prop() private msg!: string;
		firstName = "Brent";
		lastName = "Vanwildemeersch";
		get fullName() {
			return this.firstName + " " + this.lastName;
		}
	}
</script>

<style scoped>
	.qr-code-viewer-component__content {
		position: relative;
		transform: translateY(-50%);
		top: 50%;
	}
</style>