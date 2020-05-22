<template>
	<div class="qr-code-viewer-component">
		<div class="ml-8 mr-8 rounded-lg shadow-xl qr-code-viewer-component__content bg-appBlueDark">
			<img src="../../assets/qr.png" class="w-6/12 pt-20 ml-auto mr-auto" />
			<div class="mt-4 text-center content_subActions">
				<div class="inline-block w-8/12 px-4 py-2 mt-4 ml-auto mr-auto bg-orange-500 rounded-md">
					<div class="relative float-left w-9/12 text-left">
						<p>Frame</p>
					</div>
					<div class="relative float-right w-3/12">
						<AccessAlarm />
					</div>
				</div>
				<div class="inline-block w-8/12 px-4 py-2 mt-4 ml-auto mr-auto bg-orange-500 rounded-md">
					<div class="relative float-left w-9/12 text-left">
						<p>Shape & Color</p>
					</div>
					<div class="relative float-right w-3/12"></div>
				</div>
				<div class="inline-block w-8/12 px-4 py-2 mt-4 ml-auto mr-auto bg-orange-500 rounded-md">
					<div class="relative float-left w-9/12 text-left">
						<p>Logo</p>
					</div>
					<div class="relative float-right w-3/12"></div>
				</div>
			</div>
			<div class="pb-20 mt-4 text-center content-downloadActions">
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

	@Component({
		components: {}
	})
	export default class QRCodeViewerComponent extends Vue {
		@Prop() private msg!: string;
	}
</script>

<style scoped>
	.qr-code-viewer-component__content {
		position: relative;
		transform: translateY(-50%);
		top: 50%;
	}
</style>