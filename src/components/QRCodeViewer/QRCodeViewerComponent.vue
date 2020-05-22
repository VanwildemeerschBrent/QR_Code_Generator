<template>
	<div class="qr-code-viewer-component">
		<div class="m-4 qr-code-viewer-component__content bg-appBlueDark">
			<p>QR Code viewer component</p>
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
</style>